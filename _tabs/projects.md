---
title: Projects
icon: fas fa-laptop-code
order: 2
---

<style>
.project-grid {
  display: grid !important;
  grid-template-columns: repeat(auto-fit, minmax(320px, 1fr)) !important;
  gap: 32px !important;
  margin-top: 30px !important;
  width: 100%;
  max-width: 980px;
}


.project-box {
  cursor: pointer !important;
  background: #111827 !important;
  border: 1px solid #2f3b52 !important;
  border-radius: 14px !important;
  overflow: hidden !important;
  box-shadow: 0 12px 30px rgba(0,0,0,0.25) !important;
}

.project-box:hover {
  transform: translateY(-6px);
  border-color: #8ab4f8 !important;
}

.project-box img {
  width: 100% !important;
  height: 190px !important;
  object-fit: contain !important;
  background: #ffffff !important;
  padding: 24px !important;
  cursor: pointer !important;
}

.project-content {
  padding: 22px !important;
}

.project-content h3 {
  color: #ffffff !important;
  font-size: 1.1rem !important;
}

.project-content p {
  color: #c9d1d9 !important;
}

.project-period {
  color: #d1d5db !important;
  font-size: 0.85rem !important;
}

.tech-tags span {
  display: inline-block !important;
  background: #253552 !important;
  color: #8ab4f8 !important;
  border-radius: 999px !important;
  padding: 5px 11px !important;
  margin: 4px !important;
  font-size: 0.75rem !important;
  font-weight: 600 !important;
}

@media (max-width: 1024px) {
  .project-grid {
    grid-template-columns: repeat(2, 1fr) !important;
  }
}

@media (max-width: 768px) {
  .project-grid {
    grid-template-columns: 1fr !important;
  }
}
.timeline {
  position: relative;
  height: 120px;
  margin: 30px 0 60px;
  width: 100%;
  max-width: 980px;
  overflow: visible;
}


.timeline-track {
  position: absolute;
  top: 50%;
  left: 0;
  right: 0;
  height: 5px;
  background: #4b5563;
  border-radius: 999px;
}

.timeline-track::after {
  content: "";
  position: absolute;
  right: -14px;
  top: -8px;
  border-left: 18px solid #4b5563;
  border-top: 10px solid transparent;
  border-bottom: 10px solid transparent;
}

.timeline-point {
  position: absolute;
  top: 43%;
  transform: translateX(-60%);
  text-align: center;
}

.timeline-dot {
  width: 22px;
  height: 22px;
  background: #6b7280;
  border-radius: 50%;
  margin: 0 auto;
}

.timeline-label {
  margin-top: 18px;
  background: #374151;
  color: #e5e7eb;
  border-radius: 999px;
  padding: 4px 12px;
  font-size: 0.8rem;
  white-space: nowrap;
}

.hover-card {
  display: none;
  position: absolute;
  bottom: 55px;
  left: 50%;
  transform: translateX(-50%);
  width: 180px;
  background: #111827;
  border: 1px solid #2f3b52;
  border-radius: 12px;
  padding: 12px;
  box-shadow: 0 12px 30px rgba(0,0,0,0.35);
  z-index: 10;
}

.hover-card img {
  width: 100%;
  height: 90px;
  object-fit: contain;
  background: white;
  border-radius: 8px;
}

.hover-card p {
  margin: 10px 0 0;
  font-size: 0.8rem;
  color: #e5e7eb;
}

.timeline-point:hover .hover-card {
  display: block;
}

.company-marker {
  position: absolute;
  top: 5px;
  left: 50%;
  width: 13px;
  height: 13px;
  transform: translateX(-50%) rotate(45deg);
  border-radius: 2px;
  border: 1px solid rgba(255,255,255,0.35);
  z-index: 5;
}


.company-marker.ewp { background: #f59e0b; }

.company-marker.penta {
  background: #3b82f6;
}

.timeline-label.insa {
  margin-top: -55px;
  background: #374151;
  color: #e5e7eb;
  border-radius: 999px;
  padding: 4px 12px;
  font-size: 0.8rem;
  white-space: nowrap;
}
</style>

<!-- Timeline Start -->
<div class="timeline">
  <div class="timeline-track"></div>

<!-- Timeline insa point -->
<div class="timeline-point" style="left: 4%;">
    <div class="company-marker ewp"></div>
    <div class="timeline-label insa">2019.09<br>입사(동서발전)</div>
</div>
<div class="timeline-point" style="left: 24%;">
    <div class="company-marker ewp"></div>
    <div class="timeline-label insa">2021.05<br>입사(펜타시스템)</div>
</div>

<!-- Timeline project -->
  <div class="timeline-point" style="left: 14%;">
    <div class="timeline-dot"></div>
    <div class="timeline-label">2019.09<br>~2021.05</div>
  <div class="hover-card">
    <img src="/assets/img/project/ewp.png" alt="동서발전">
    <p>동서발전 임시직</p>
  </div>
</div>

  <div class="timeline-point" style="left: 34%;">
    <div class="timeline-dot"></div>
    <div class="timeline-label">2021.05<br>~2021.10</div>
    <div class="hover-card">
    <img src="/assets/img/project/ewp.png" alt="동서발전">
    <p>DW사업 유지보수</p>
  </div>
</div>

  <div class="timeline-point" style="left: 44%;">
    <div class="timeline-dot"></div>
    <div class="timeline-label">2021.10<br>~2022.01</div>
    <div class="hover-card">
    <img src="/assets/img/project/kcg.png" alt="해양경찰청">
    <p>빅데이터통합저장소 2단계 구축</p>
  </div>
</div>

  <div class="timeline-point" style="left: 54%;">
    <div class="timeline-dot"></div>
    <div class="timeline-label">2022.01<br>~2022.04</div>
    <div class="hover-card">
    <img src="/assets/img/project/ewp.png" alt="동서발전">
    <p>지능형 디지털 발전소 플랫폼 구축</p>
  </div>
</div>

  <div class="timeline-point" style="left: 64%;">
    <div class="timeline-dot"></div>
    <div class="timeline-label">2022.05<br>~2022.12</div>
    <div class="hover-card">
    <img src="/assets/img/project/kcg.png" alt="해양경찰청">
    <p>데이터 통합저장소 3단계 구축</p>
  </div>
</div>
  <div class="timeline-point" style="left: 74%;">
    <div class="timeline-dot"></div>
    <div class="timeline-label">2023.02<br>~2023.10</div>
    <div class="hover-card">
    <img src="/assets/img/project/kwater.png" alt="수자원공사">
    <p>스마트 정수장 구축 사업</p>
  </div>
</div>

  <div class="timeline-point" style="left: 84%;">
    <div class="timeline-dot"></div>
    <div class="timeline-label">2023.11<br>~2025.03</div>
    <div class="hover-card">
    <img src="/assets/img/project/busan.png" alt="부산시청">
    <p>부산형 데이터 통합플랫폼 구축</p>
  </div>
</div>

  <div class="timeline-point" style="left: 94%;">
    <div class="timeline-dot"></div>
    <div class="timeline-label">2025.08<br>~2026.04</div>
    <div class="hover-card">
    <img src="/assets/img/project/gyeonggi.png" alt="경기도교육청">
    <p>경기 교육 디지털플랫폼 구축</p>
  </div>
</div>
</div>


<div class="project-grid">

  <div class="project-box" onclick="location.href='/projects/gyeonggi-edu/'">
    <img src="/assets/img/project/gyeonggi.png" alt="경기교육 디지털플랫폼">

    <div class="project-content">
      <h3>경기도 교육청</h3>
      <p>경기교육 디지털플랫폼 구축</p>

      <p class="project-period">
        📅 2025.08.01 ~ 2026.04.17
      </p>

      <div class="tech-tags">
	    <span>Data Engineer</span>
        <span>Python</span>
        <span>GreenplumDB</span>
		<span>Hadoop Eco</span>
        <span>TeraStream</span>
		<span>API 수집/적재</span>
		<span>비정형 데이터 수집/적재</span>
      </div>
    </div>
  </div>

  <div class="project-box" onclick="location.href='/projects/busan-cityhall/'">
    <img src="/assets/img/project/busan.png" alt="부산형 데이터 통합플랫폼 구축">

    <div class="project-content">
      <h3>부산시청</h3>
      <p>부산형 데이터 통합플랫폼 구축</p>

      <p class="project-period">
        📅 2023.11.01 ~ 2025.03.31
      </p>

      <div class="tech-tags">
        <span>Data Engineer</span>
		<span>Python</span>
        <span>계보관리</span>
        <span>PostgreSQL</span>
		<span>Hadoop Eco</span>
		<span>API 수집/적재</span>
		<span>정형/비정형 수집/적재</span>
      </div>
    </div>
  </div>

  <div class="project-box" onclick="location.href='/projects/kwater/'">
    <img src="/assets/img/project/kwater.png" alt="스마트 정수장 구축 사업">
    <div class="project-content">
      <h3>한국수자원공사</h3>
      <p>금강북부 스마트 정수장 구축 사업</p>

      <p class="project-period">
        📅 2023.02.13 ~ 2023.10.27
      </p>

      <div class="tech-tags">
	    <span>TA</span>
        <span>Python</span>
        <span>Docker Swarm</span>
        <span>MariaDB</span>
		<span>Galera Cluster</span>
		<span>Kafka</span>
		<span>NIFI</span>
		<span>FluentD</span>
		<span>Metrix/File beat</span>
		<span>보안 취약점 점검 및 조치</span>
      </div>
    </div>
  </div>

  <div class="project-box" onclick="location.href='/projects/kcg/'">
    <img src="/assets/img/project/kcg.png" alt="데이터 통합저장소 3단계 구축">
    <div class="project-content">
      <h3>해양경찰청</h3>
      <p>데이터 통합저장소 3단계 구축</p>

      <p class="project-period">
        📅 2022.05.25 ~ 2022.12.24
      </p>

      <div class="tech-tags">
	    <span>TA</span>
        <span>ShellScript</span>
        <span>API 서버 구축</span>
        <span>PostgreSQL</span>
		<span>JBOSS</span>
		<span>JBCS</span>
		<span>이중화 구성</span>
		<span>웹서비스 코드 수정</span>
		<span>보안 취약점 점검 및 조치</span>
      </div>
    </div>
  </div>
  
<div class="project-box" onclick="location.href='/projects/ewp/'">
    <img src="/assets/img/project/ewp.png" alt="지능형 디지털 발전소 플랫폼 구축">
    <div class="project-content">
      <h3>한국동서발전</h3>
      <p>지능형 디지털 발전소 플랫폼 구축</p>

      <p class="project-period">
        📅 2022.01.24 ~ 2022.04.22
      </p>

      <div class="tech-tags">
	    <span>TA</span>
        <span>ShellScript</span>
		<span>Openstack 구축</span>
        <span>MariaDB</span>
        <span>PostgreSQL</span>
		<span>JBOSS</span>
		<span>JBCS</span>
		<span>이중화 구성</span>
		<span>네트워크 구성</span>
		<span>보안 취약점 점검 및 조치</span>
      </div>
    </div>
  </div>

<div class="project-box" onclick="location.href='/projects/kcg/'">
    <img src="/assets/img/project/kcg.png" alt="빅데이터통합저장소 2단계 구축">
    <div class="project-content">
      <h3>해양경찰청</h3>
      <p>빅데이터통합저장소 2단계 구축</p>

      <p class="project-period">
        📅 2021.10.14 ~ 2022.01.14
      </p>

      <div class="tech-tags">
	    <span>TA</span>
        <span>ShellScript</span>
		<span>Server 환경 구축(GIS, WEB, WAS, Tableau 등)</span>
        <span>PostgreSQL</span>
		<span>Hadoop Eco</span>
		<span>Tableau</span>
		<span>이중화 구성</span>
		<span>네트워크 구성</span>
		<span>보안 취약점 점검 및 조치</span>
      </div>
    </div>
  </div>

<div class="project-box" onclick="location.href='/projects/ewp/'">
    <img src="/assets/img/project/ewp.png" alt="DW 사업 유지보수">
    <div class="project-content">
      <h3>한국동서발전</h3>
      <p>DW 사업 유지보수</p>

      <p class="project-period">
        📅 2021.05.17 ~ 2021.10.11
      </p>

      <div class="tech-tags">
	    <span>유지보수</span>
        <span>ShellScript</span>
		<span>Log 분석</span>
        <span>MongoDB</span>
        <span>PostgreSQL</span>
		<span>API/정형/비정형</span>
		<span>네트워크 환경 점검</span>
		<span>보안 취약점 점검 및 조치</span>
      </div>
    </div>
  </div>

<div class="project-box" onclick="location.href='/projects/ewp/'">
    <img src="/assets/img/project/ewp.png" alt="시스템 구축 및 운영, 시각화, 데이터베이스">
    <div class="project-content">
      <h3>한국동서발전</h3>
      <p>동서발전 임시직(디지털기술융합원 솔루션개발부)</p>

      <p class="project-period">
        📅 2019.09 ~ 2021.05
      </p>

      <div class="tech-tags">
	    <span>빅데이터 포털 운영</span>
        <span>데이터 분석 과제 페이지 구축</span>
		<span>Tableau 시각화</span>
        <span>PostgreSQL</span>
		<span>Tibero</span>
		<span>Oracle</span>
      </div>
    </div>
  </div>
  
</div>