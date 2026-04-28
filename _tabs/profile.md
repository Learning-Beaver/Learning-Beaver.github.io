---
# the default layout is 'page'
title: Profile
icon: fas fa-id-card
order: 1
---

<style>
.business-card {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  max-width: 860px;
  margin: 40px auto;
  background: #f8f8f8;
  color: #222;
  border: 1px solid #d1d5db;
  box-shadow: 12px 12px 0 rgba(0,0,0,0.08);
  border-radius: 6px;
  padding: 40px;
  position: relative;
}

.company-logo {
  position: absolute;
  top: -10px;
  right: 30px;
  width: 248px;
  height: 102px;
  object-fit: contain;
}

.left-section {
  width: 38%;
}

.right-section {
  width: 52%;
  margin-top: 55px;
  margin-left: auto;
}

.business-card .role {
  margin-top: 40px;
  font-size: 1.05rem;
  color: #555;
  line-height: 1.6;
}

.business-card .name {
  font-size: 2.7rem;
  font-weight: 800;
  letter-spacing: 8px;
  margin: 14px 0 34px;
}

.business-card .info {
  font-size: 1.05rem;
  line-height: 1.8;
}

.section-title {
  font-weight: 800;
  margin-bottom: 10px;
  color: #111;
}

.project-list p {
  margin: 5px 0;
  font-size: 0.92rem;
  color: #333;
  line-height: 1.55;
}

.skill-summary {
  margin-top: 18px;
}

.skill-detail {
  margin-top: 12px;
}

.skill-detail summary {
  cursor: pointer;
  font-size: 0.82rem;
  font-weight: 800;
  color: #1e3a8a;
  margin-bottom: 8px;
}

.skill-group {
  margin-top: 10px;
}

.group-title {
  font-size: 0.72rem;
  font-weight: 800;
  color: #333;
  margin-bottom: 5px;
}

.skill-tags span,
.skill-summary span {
  display: inline-block;
  background: #1e3a8a;
  color: white;
  border-radius: 999px;
  padding: 5px 10px;
  margin: 3px;
  font-size: 0.75rem;
  font-weight: 700;
}

@media (max-width: 768px) {
  .business-card {
    flex-direction: column;
  }

  .left-section,
  .right-section {
    width: 100%;
  }

  .right-section {
    margin-top: 30px;
  }

  .company-logo {
    position: static;
    width: 180px;
    height: auto;
    margin-left: auto;
    display: block;
  }
}
</style>


<h2 style="margin-top:60px;">2026.01.01 ~ </h2>
<div class="business-card">
  <img src="/assets/img/business-card/penta.png" class="company-logo" alt="PENTA 로고">

  <div class="left-section">
    <div class="role">SI Data Analytics Team 책임</div>
    <div class="name">김 재 현</div>

    <div class="info">
      DE(Data Engineer)
    </div>
  </div>

  <div class="right-section">
    <div class="section-title">참여 사업</div>

    <div class="project-list">
      <p>• 경기도교육청 경기교육 디지털플랫폼 구축 (DE)</p>
    </div>

    <div class="skill-summary">
  <span>Linux</span>
  <span>Hadoop Ecosystem</span>
  <span>GPDB</span>
  <span>Python</span>
  <span>정형/비정형</span>
  <span>Shell Script</span>
</div>

<details class="skill-detail">
  <summary>기술 스택 더보기</summary>

  <div class="skill-group">
    <div class="group-title">OS / Infra</div>
    <div class="skill-tags">
      <span>Platform Engineering</span>
      <span>Network Architect</span>
    </div>
  </div>

  <div class="skill-group">
    <div class="group-title">Data / ETL</div>
    <div class="skill-tags">
       <span>TeraStream</span>
	   <span>API</span>
    </div>
  </div>

  <div class="skill-group">
    <div class="group-title">DB</div>
    <div class="skill-tags">
      <span>PostgreSQL</span>
	  <span>DB2</span>
	  <span>MySQL</span>
      <span>SQL Query</span>
    </div>
  </div>
</details>
  </div>
</div>


<h2 style="margin-top:60px;">2023.01.01 ~ 2025.12.31</h2>
<div class="business-card">
  <img src="/assets/img/business-card/penta.png" class="company-logo" alt="PENTA 로고">

  <div class="left-section">
    <div class="role">Blue Analytics<br> Data Platform Team 전임</div>
    <div class="name">김 재 현</div>

    <div class="info">
      TA(Technical Architect) <br>
      & DE(Data Engineer)
    </div>
  </div>

  <div class="right-section">
    <div class="section-title">참여 사업</div>

    <div class="project-list">
      <p>• 수자원공사 금강북부 스마트정수장 구축 (TA)</p>
      <p>• 부산시청 부산형 데이터 통합플랫폼 구축 (DE)</p>
    </div>

    <div class="skill-summary">
  <span>Linux</span>
  <span>Docker Swarm</span>
  <span>Kafka</span>
  <span>PostgreSQL</span>
  <span>Python</span>
  <span>Platform Engineering</span>
</div>

<details class="skill-detail">
  <summary>기술 스택 더보기</summary>

  <div class="skill-group">
    <div class="group-title">OS / Infra</div>
    <div class="skill-tags">
      <span>Hadoop Ecosystem</span>
      <span>OpenStack</span>
      <span>Service HA</span>
      <span>Network Architect</span>
      <span>Tableau</span>
    </div>
  </div>

  <div class="skill-group">
    <div class="group-title">Data / ETL</div>
    <div class="skill-tags">
      <span>Nifi</span>
      <span>FluentD</span>
      <span>Metricbeat</span>
      <span>Filebeat</span>
      <span>정형/비정형</span>
      <span>API</span>
    </div>
  </div>

  <div class="skill-group">
    <div class="group-title">DB</div>
    <div class="skill-tags">
      <span>Tibero</span>
      <span>Oracle</span>
      <span>PostgreSQL</span>
      <span>SQL Query</span>
    </div>
  </div>

  <div class="skill-group">
    <div class="group-title">Programming / Security</div>
    <div class="skill-tags">
      <span>Shell Script</span>
      <span>JavaScript</span>
      <span>취약점 점검 및 조치</span>
    </div>
  </div>
</details>

  </div>
</div>


<h2 style="margin-top:60px;">2021.09.17 ~ 2022.12.31</h2>
<div class="business-card">
  <img src="/assets/img/business-card/penta.png" class="company-logo" alt="PENTA 로고">

  <div class="left-section">
    <div class="role">Big Data Team 사원</div>
    <div class="name">김 재 현</div>

    <div class="info">
      TA(Technical Architect)
    </div>
  </div>

  <div class="right-section">
    <div class="section-title">참여 사업</div>

    <div class="project-list">
      <p>• 한국동서발전 DW 사업 유지보수</p>
      <p>• 해양경찰청 빅데이터 통합저장소 2단계 구축</p>
      <p>• 동서발전 EWP 지능형 디지털 발전소 플랫폼 구축</p>
      <p>• 해양경찰청 데이터 통합저장소 3단계 구축</p>
    </div>
	    <div class="skill-summary">
  <span>Linux</span>
  <span>Hadoop EcoSystem</span>
  <span>Tableau Server</span>
  <span>PostgreSQL</span>
  <span>Python</span>
  <span>Platform Engineering</span>
</div>

<details class="skill-detail">
  <summary>기술 스택 더보기</summary>

  <div class="skill-group">
    <div class="group-title">OS / Infra</div>
    <div class="skill-tags">
      <span>RHEL</span>
      <span>OpenStack</span>
      <span>Service HA</span>
      <span>Network Architect</span>
      <span>Infrastructure Engineering</span>
    </div>
  </div>

  <div class="skill-group">
    <div class="group-title">Data Platform</div>
    <div class="skill-tags">
      <span>Hadoop Ecosystem</span>
       <span>Tableau</span>
    </div>
  </div>

  <div class="skill-group">
    <div class="group-title">DB</div>
    <div class="skill-tags">
      <span>Tibero</span>
      <span>Oracle</span>
      <span>SQL Query</span>
    </div>
  </div>

  <div class="skill-group">
    <div class="group-title">Programming / Security</div>
    <div class="skill-tags">
      <span>Shell Script</span>
      <span>JavaScript</span>
      <span>취약점 점검 및 조치</span>
    </div>
  </div>
</details>

  </div>
</div>



<h2 style="margin-top:60px;">2019.09.17 ~ 2021.05.14</h2>
<div class="business-card">
  <img src="/assets/img/business-card/ewp.png" class="company-logo" alt="EWP 로고">

  <div class="left-section">
    <div class="role">솔루션개발부 [임시직]</div>
    <div class="name">김 재 현</div>

    <div class="info">
      시스템 구축 및 운영 <br>
      시각화 및 데이터베이스 관리
    </div>
  </div>

  <div class="right-section">
    <div class="section-title">주요 업무</div>

    <div class="project-list">
      <p>• 시스템 구축 및 운영</p>
      <p>• 데이터 시각화</p>
      <p>• 데이터베이스 관리</p>
    </div>
	    <div class="skill-summary">
  <span>Linux</span>
  <span>Hadoop EcoSystem</span>
  <span>Tableau</span>
  <span>PostgreSQL</span>
  <span>Tibero</span>
  <span>Shell Script</span>
</div>

<details class="skill-detail">
  <summary>기술 스택 더보기</summary>
  <div class="skill-group">
    <div class="group-title">OS / Infra</div>
    <div class="skill-tags">
      <span>RHEL</span>
    </div>
  </div>
  <div class="skill-group">
    <div class="group-title">DB</div>
    <div class="skill-tags">
      <span>Oracle</span>
      <span>SQL Query</span>
    </div>
  </div>

  <div class="skill-group">
    <div class="group-title">Programming</div>
    <div class="skill-tags">
      <span>JavaScript</span>
      <span>Python</span>
	  <span>visual basic</span>
    </div>
  </div>
</details>
  </div>
</div>