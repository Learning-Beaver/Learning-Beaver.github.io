---
title: Projects
icon: fas fa-laptop-code
order: 5
---
<style>
.project-grid {
  display: grid !important;
  grid-template-columns: repeat(3, minmax(300px, 1fr)) !important;
  gap: 32px !important;
  margin-top: 30px !important;
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
</style>

<div class="project-grid">

  <div class="project-box" onclick="location.href='/projects/gyeonggi-platform/'">
    <img src="/assets/img/project/gyeonggi.png" alt="경기교육 디지털플랫폼">

    <div class="project-content">
      <h3>경기교육 디지털플랫폼 구축</h3>
      <p>통합데이터 저장소 및 학습데이터 저장소 구축</p>

      <p class="project-period">
        📅 2025.08.01 ~ 2026.04.17
      </p>

      <div class="tech-tags">
        <span>GPDB</span>
        <span>ETL</span>
        <span>AI</span>
      </div>
    </div>
  </div>

  <div class="project-box" onclick="location.href='/projects/gyeonggi-platform/'">
    <img src="/assets/img/project/busan.png" alt="부산형 데이터 통합플랫폼 구축">

    <div class="project-content">
      <h3>부산형 데이터 통합플랫폼 구축</h3>
      <p>데이터 수집·적재·통합 플랫폼 구축</p>

      <p class="project-period">
        📅 2023.11.01 ~ 2025.03.31
      </p>

      <div class="tech-tags">
        <span>ETL</span>
        <span>계보관리</span>
        <span>DW</span>
		<span>Hadoop Eco</span>
		<span>Python</span>
      </div>
    </div>
  </div>



</div>