---
title: "Object Storage 기반 데이터 플랫폼 구축기 #1 - 프로젝트를 시작하며"
date: 2026-06-22 23:45:00 +0900
categories: [Personal-Project]
tags: [MinIO, Iceberg, Hive, Hue, Airflow, NiFi, Lakehouse]
---

# 프로젝트를 시작하며

최근 데이터 플랫폼 아키텍처를 살펴보면 과거 Hadoop 중심의 구조에서 Object Storage 기반 구조로 빠르게 변화하고 있다.

과거에는 HDFS를 중심으로 Hive, Spark, HBase 등을 구성하는 것이 일반적이었다.

```text
Source
  ↓
 HDFS
  ↓
 Hive
  ↓
 Analytics
```

하지만 최근에는 AWS S3, Azure Data Lake Storage, Google Cloud Storage와 같은 Object Storage가 사실상 데이터 레이크의 표준 저장소로 자리잡고 있다.

여기에 Apache Iceberg, Delta Lake, Apache Hudi와 같은 오픈 테이블 포맷(Open Table Format)이 등장하면서 기존 Hadoop 아키텍처를 반드시 사용해야 할 이유도 점차 줄어들고 있다.

문득 이런 생각이 들었다.

> "과연 Hadoop 없이도 실무 수준의 데이터 플랫폼을 구축할 수 있을까?"

이번 프로젝트는 이 질문에 대한 답을 찾기 위해 시작하게 되었다.

---

# 프로젝트 목표

이번 프로젝트의 목표는 Hadoop Cluster 없이 데이터 플랫폼을 구축하고 운영하는 것이다.

단순히 기술을 설치하는 것이 목적은 아니다.

다음과 같은 항목들을 직접 검증해 보고자 한다.

* Object Storage 기반 데이터 레이크 구축
* Iceberg 기반 ACID Transaction 지원
* Hive를 통한 메타데이터 및 SQL 조회
* Hue 기반 사용자 분석 환경 제공
* Airflow 기반 워크플로우 관리
* NiFi 기반 데이터 수집 및 적재
* Hadoop 없이 Lakehouse 아키텍처 구현

---

# 왜 Hadoop을 사용하지 않을까?

Hadoop은 여전히 훌륭한 플랫폼이다.

하지만 최근 데이터 플랫폼은 저장소와 처리 엔진이 점차 분리되고 있다.

예전에는 다음과 같은 구조가 일반적이었다.

```text
Storage + Metadata + Compute
          │
       Hadoop
```

반면 최근에는

```text
Object Storage
       │
    Iceberg
       │
 Hive / Spark / Trino
```

와 같은 구조가 점점 늘어나고 있다.

특히 Object Storage는 사실상 무제한 확장이 가능하고 운영이 단순하며 다양한 분석 엔진과 쉽게 연계할 수 있다는 장점이 있다.

---

# 이번 프로젝트에서 사용할 기술

## MinIO

이번 프로젝트의 핵심 저장소이다.

MinIO는 S3 API를 지원하는 오픈소스 Object Storage이다.

최근 대부분의 데이터 엔진들이 S3 프로토콜을 지원하기 때문에 HDFS 대신 MinIO를 데이터 저장소로 활용할 예정이다.

---

## Apache Iceberg

Object Storage만으로는 부족하다.

실무 환경에서는 다음과 같은 기능이 필요하다.

* UPDATE
* DELETE
* MERGE
* Time Travel
* Schema Evolution

기존 Hive External Table만으로는 이러한 기능을 제공하기 어렵다.

Iceberg는 이러한 문제를 해결하기 위해 등장한 오픈 테이블 포맷이며, Object Storage 위에서 ACID Transaction을 지원한다.

이번 프로젝트에서는 Iceberg를 통해 Lakehouse 구조를 구현할 예정이다.

---

## Hive

Hive는 메타스토어와 SQL 인터페이스 역할을 담당한다.

Iceberg Catalog와 연동하여 데이터 조회 및 메타데이터 관리를 수행할 예정이다.

---

## Hue

사용자 SQL 분석 환경을 제공한다.

웹 브라우저에서 손쉽게 데이터를 조회하고 분석할 수 있도록 구성할 예정이다.

---

## Apache Airflow

배치 워크플로우 관리 도구이다.

데이터 적재, 가공, 검증 작업을 DAG 형태로 관리할 예정이다.

---

## Apache NiFi

데이터 수집 및 데이터 흐름 관리를 담당한다.

파일, API, DB 등 다양한 데이터 소스로부터 데이터를 수집하여 MinIO에 적재하는 역할을 수행할 예정이다.

---

# 최종 목표 아키텍처

최종적으로는 아래와 같은 구조를 목표로 한다.

```text
                 +-------------+
                 |    NiFi     |
                 +------+------+
                        |
                        v

+--------------------------------------------------+
|                    MinIO                         |
|               (Object Storage)                   |
+--------------------------------------------------+
                        |
                        v

                 +-------------+
                 |   Iceberg   |
                 +------+------+
                        |
                        v

           +------------+------------+
           |                         |
           v                         v

        Hive                     Spark
           \                       /
            \                     /
             +-----------------+
             |       Hue       |
             +-----------------+

                        ^
                        |
                 +-------------+
                 |   Airflow   |
                 +-------------+
```

---

# 이번 프로젝트에서 확인하고 싶은 것

이번 프로젝트를 통해 다음 내용을 직접 검증할 계획이다.

* MinIO는 HDFS를 어느 수준까지 대체할 수 있는가?
* Hive와 Iceberg 조합은 실무에서 사용 가능한가?
* Object Storage 기반 Lakehouse 구조는 얼마나 단순한가?
* Airflow와 NiFi를 활용한 데이터 파이프라인 운영은 가능한가?
* 소규모 조직에서도 운영 가능한 데이터 플랫폼을 만들 수 있는가?

---

# 마치며

이번 프로젝트는 단순한 설치 실습이 아니다.

최근 데이터 플랫폼이 Hadoop 중심 구조에서 Object Storage 기반 Lakehouse 구조로 전환되고 있는 흐름을 직접 검증해 보는 과정이다.

다음 글에서는 전체 아키텍처 설계와 서버 구성을 정리해 보려고 한다.
