<template>
  <div class="about-section">
    <div class="container">
      <h2 class="section-title">Sobre Mí</h2>
      
      <div class="about-grid">
        <div class="about-text">
          <p>
            Egresado de Ingeniería Estadística e Informática con experiencia en análisis de datos, 
            elaboración de dashboards de seguimiento y reportes ejecutivos para toma de decisiones. 
            Manejo de Excel, SQL, Power BI, Python y herramientas de Microsoft Office aplicadas al análisis y visualización de datos. 
            Experiencia adicional en automatización de procesos y desarrollo de soluciones digitales, 
            con capacidad de trabajo en equipo y adaptación a distintos entornos técnicos e institucionales.
          </p>
        </div>
        
        <div class="about-details">
          <div class="detail-box">
            <h3>Educación</h3>
            <ul>
              <li>
                <strong>Universidad Nacional del Altiplano Puno</strong><br />
                Ingeniería Estadística e Informática — Egresado | 2021 -- 2025
              </li>
              <li>
                <strong>Instituto de Informática (UNAP)</strong><br />
                Diplomado en Ciencia de Datos | Técnico en Ofimática
              </li>
              <li>
                <strong>Instituto de Idiomas (UNAP)</strong><br />
                Inglés Intermedio B2
              </li>
            </ul>
          </div>
          
          <div class="detail-box cert-box">
            <h3>Certificados Destacados</h3>
            <ul>
              <li><strong>Ethical Hacker</strong><br />Cisco Networking Academy</li>
              <li><strong>Microsoft Power BI, Excel Avanzado, SQL Server Intermedio</strong><br />WE Educación Ejecutiva</li>
              <li><strong>Introduction to Data Science, Python Essentials 2, Ciberseguridad</strong><br />Cisco Networking Academy</li>
              <li><strong>Modelado de Datos con Python G8</strong><br />Alura Latam / ONE</li>
              <li><strong>Diplomado en Gestión de Servicios de TI con ITIL v5</strong><br />CETI</li>
            </ul>
          </div>

          <div class="detail-box">
            <h3>Habilidades Técnicas</h3>
            <div class="skills-tags">
              <span>Python</span>
              <span>R</span>
              <span>SQL</span>
              <span>Power BI</span>
              <span>Excel Avanzado</span>
              <span>FastAPI</span>
              <span>Django</span>
              <span>Vue.js</span>
              <span>React</span>
              <span>Machine Learning</span>
              <span>Docker</span>
              <span>Git</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use '../styles/variables.scss' as *;

.about-section {
  width: 100%;
  padding: 4rem 2rem;
  box-sizing: border-box;
  background-color: rgba(0, 0, 0, 0.03);
}

.container {
  max-width: 1400px;
  margin: 0 auto;
}

.section-title {
  font-size: 2.5rem;
  color: $color-accent;
  text-transform: uppercase;
  letter-spacing: 2px;
  margin-bottom: 3rem;
  border-bottom: 2px solid $color-accent-2;
  padding-bottom: 0.5rem;
  display: inline-block;
}

.about-grid {
  display: grid;
  grid-template-columns: 1.2fr 1fr;
  gap: 4rem;
  
  @media (max-width: 1024px) {
    grid-template-columns: 1fr;
    gap: 2rem;
  }
}

.about-text {
  p {
    font-size: 1.1rem;
    line-height: 1.8;
    color: rgba($color-body, 0.9);
    text-align: justify;
  }
}

.about-details {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.detail-box {
  background: rgba($color-surface-light, 0.9);
  padding: 1.5rem;
  border: 1px solid rgba($color-accent, 0.3);
  /* BORDES RECTOS */
  
  h3 {
    margin-top: 0;
    color: $color-accent;
    text-transform: uppercase;
    font-size: 1.2rem;
    margin-bottom: 1rem;
  }
  
  ul {
    list-style: none;
    padding: 0;
    margin: 0;
    
    li {
      margin-bottom: 1rem;
      font-size: 0.95rem;
      line-height: 1.4;
      color: rgba($color-body, 0.8);
      
      strong {
        color: $color-heading;
      }
      
      &:last-child {
        margin-bottom: 0;
      }
    }
  }
}

.cert-box {
  ul li {
    margin-bottom: 0.8rem;
    font-size: 0.95rem;
    color: rgba($color-body, 0.9);
  }
}

.skills-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
  
  span {
    background: rgba($color-accent, 0.1);
    color: $color-heading;
    padding: 0.4rem 0.8rem;
    font-size: 0.85rem;
    border: 1px solid rgba($color-accent, 0.5);
    /* BORDES RECTOS */
  }
}
</style>
