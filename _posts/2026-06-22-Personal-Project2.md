---
title: "Object Storage 기반 데이터 플랫폼 구축기 #2 - 왜 MinIO와 Iceberg를 선택했을까?"
date: 2026-06-23 23:05:00 +0900
categories: [Personal-Project]
tags: [MinIO, Iceberg, Lakehouse, ObjectStorage]
---

# 왜 MinIO와 Iceberg를 선택했을까?

이전 글에서는 Hadoop 없이 데이터 플랫폼을 구축하려는 이유와 전체 목표를 소개했다.

이번 글에서는 프로젝트의 핵심 기술인 MinIO와 Iceberg를 선택한 이유를 정리해보려고 한다.

---

# 먼저 고민했던 것

이번 프로젝트를 설계하면서 가장 먼저 고민한 것은 저장소였다.

전통적인 Hadoop 환경이라면 자연스럽게 HDFS를 선택했을 것이다.

```text
Data Source
      ↓
     HDFS
      ↓
     Hive
      ↓
   Analytics
```

하지만 이번 프로젝트는 Hadoop Cluster를 운영하지 않는 것이 목표였다.

그렇다면 저장소는 무엇으로 대체할 수 있을까?

---

# Object Storage라는 선택

최근 클라우드 환경에서는 대부분 Object Storage를 사용한다.

대표적으로

* AWS S3
* Azure Data Lake Storage
* Google Cloud Storage

등이 있다.

이들은 모두 Object Storage라는 공통된 구조를 사용한다.

Object Storage는 파일을 객체(Object) 단위로 저장하며 다음과 같은 특징을 가진다.

* 높은 확장성
* 저렴한 저장 비용
* 단순한 구조
* REST API 기반 접근

즉,

과거의

```text
HDFS
```

대신

```text
Object Storage
```

를 사용할 수 있게 된 것이다.

---

# MinIO를 선택한 이유

Object Storage를 구축하는 방법은 여러 가지가 있다.

대표적으로는

* AWS S3
* NHN Object Storage
* MinIO
* Ceph

등이 있다.

이번 개인 프로젝트에서는 MinIO를 선택했다.

이유는 단순했다.

여러번 구성해 보았기 때문에, S3 API를 완벽히 호환해서

개인 프로젝트에서 가장 빠르게 환경을 구축하고, 향후 AWS S3 버킷을 활용할 때에도 문제가 없다 라는 이유이다.

MinIO는 다음과 같은 장점을 제공한다.

* S3 API 완벽 호환
* Docker 기반 구축 가능
* 설치 및 운영 단순
* 높은 성능
* 활발한 오픈소스 커뮤니티

특히 Hive, Spark, Trino, Airflow 등 대부분의 데이터 플랫폼 솔루션이 S3 API를 지원하기 때문에 MinIO는 실습 환경에 매우 적합하다.

---

# 하지만 Object Storage만으로는 부족하다

여기서 문제가 하나 생긴다.

Object Storage는 데이터를 저장하는 공간일 뿐이다.

예를 들어 CSV 파일을 저장할 수는 있지만 다음 기능은 제공하지 않는다.

* UPDATE
* DELETE
* MERGE
* Time Travel
* ACID Transaction

데이터 웨어하우스에서는 너무나 당연한 기능들이지만 Object Storage 자체로는 지원되지 않는다.

---

# 그래서 Iceberg가 필요하다

Apache Iceberg는 Object Storage 위에서 동작하는 오픈 테이블 포맷(Open Table Format)이다.

쉽게 말하면

```text
Object Storage
+
데이터 관리 계층
=
Iceberg
```

라고 생각할 수 있다.

Iceberg는 다음 기능을 제공한다.

* ACID Transaction
* Time Travel
* Snapshot 관리
* Schema Evolution
* Partition 관리

이를 통해 Object Storage를 단순 저장소가 아닌 데이터 플랫폼 저장소로 활용할 수 있게 된다.

---

# 내가 생각하는 역할 분담

이번 프로젝트에서는 각 컴포넌트의 역할을 다음과 같이 정의했다.

```text
MinIO
=
데이터 저장

Iceberg
=
데이터 관리

Hive
=
메타데이터 및 SQL

Hue
=
사용자 분석 환경

Airflow
=
워크플로우 관리

NiFi
=
데이터 수집
```

즉,

각 컴포넌트가 하나의 역할에 집중하도록 설계하는 것이다.

---

# 최종적으로 만들고 싶은 구조

이번 프로젝트의 최종 목표는 아래 구조이다.

```text
Data Source
      ↓
     NiFi
      ↓
    MinIO
      ↓
   Iceberg
      ↓
     Hive
      ↓
      Hue

Airflow
   ↓
전체 파이프라인 관리
```

이 구조가 실제 Hadoop 기반 플랫폼을 어느 수준까지 대체할 수 있는지 직접 검증해 볼 예정이다.

---

# 다음 글

다음 글에서는 실제 구축을 시작하기 전에 전체 서버 구성과 Docker 기반 아키텍처를 설계해 보려고 한다.

특히 Hive Metastore와 Iceberg Catalog를 어떤 방식으로 연결할 것인지도 함께 정리할 예정이다.
