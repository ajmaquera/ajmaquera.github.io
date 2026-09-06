<template>
  <div class="experience-section">
    <div class="container">
      <h2 class="section-title">Experiencia</h2>
      
      <div class="timeline">
        <div class="timeline-item">
          <div class="timeline-date">Mayo. -- Jul. 2026</div>
          <div class="timeline-content">
            <h3>Asistente de Sistemas y Soporte Electoral</h3>
            <h4>Universidad Nacional del Altiplano -- Comité Electoral Universitario | Puno, Perú</h4>
            <ul>
              <li>Elaboré reportes y brindé soporte de seguimiento al proceso electoral, incluyendo diseño y revisión de cédulas, organización de material, atención a usuarios y apoyo en el escrutinio y conteo de votos.</li>
              <li>Desarrollé una plataforma web de consulta electoral y un sistema de gestión de actas con carga de fotografías mediante app móvil Android y validación desde panel administrativo.</li>
            </ul>
          </div>
        </div>
        
        <div class="timeline-item">
          <div class="timeline-date">Feb. -- Jun. 2026</div>
          <div class="timeline-content">
            <h3>Desarrollador Full Stack Junior</h3>
            <h4>Universidad Nacional del Altiplano -- OTI | Puno, Perú</h4>
            <ul>
              <li>Diseñé reportes estadísticos periódicos sobre distribución y categorías del personal docente y no docente, y participé en la elaboración del Plan de Gobierno Digital institucional.</li>
              <li>Desarrollé el Sistema de Escalafón de RRHH para gestión de personal, implementando flujos con firmas digitales en el marco de la transformación digital.</li>
            </ul>
          </div>
        </div>

        <div class="timeline-item">
          <div class="timeline-date">Ago. -- Dic. 2025</div>
          <div class="timeline-content">
            <h3>Analista de Datos y Desarrollador Web (Pre Profesional)</h3>
            <h4>Universidad Nacional del Altiplano -- OTI | Puno, Perú</h4>
            <ul>
              <li>Monitoreé indicadores de desempeño del chatbot institucional desde un panel administrativo, generando reportes para optimizar el modelo.</li>
              <li>Desarrollé chatbot institucional con arquitectura RAG basada en el modelo local Qwen, automaticé procesos web con scripts en Python y contribuí al Plan de Seguridad de la Información.</li>
            </ul>
          </div>
        </div>
        
        <div class="timeline-item">
          <div class="timeline-date">Ene. -- Abr. 2025</div>
          <div class="timeline-content">
            <h3>Asistente de Desarrollo Backend y Analista de Datos</h3>
            <h4>Fatcbrands (Remoto) | Bogotá, Colombia</h4>
            <ul>
              <li>Apliqué análisis estadístico de datos con Python para reportes internos de apoyo a decisiones, además de desarrollar y desplegar aplicaciones backend con Django en VPS/Linux.</li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use '../styles/variables.scss' as *;

.experience-section {
  width: 100%;
  padding: 4rem 2rem;
  box-sizing: border-box;
  background-color: transparent;
}

.container {
  max-width: 1200px;
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

.timeline {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.timeline-item {
  display: flex;
  gap: 2rem;
  background: rgba($color-surface-light, 0.9);
  border: 1px solid rgba($color-accent, 0.3);
  /* BORDES RECTOS */
  border-radius: 0; 
  padding: 1.5rem;
  transition: border-color 0.3s ease, background 0.3s ease;
  
  &:hover {
    border-color: $color-accent;
    background: rgba($color-surface-light, 1);
  }
  
  @media (max-width: 768px) {
    flex-direction: column;
    gap: 1rem;
  }
}

.timeline-date {
  min-width: 150px;
  color: $color-accent-2;
  font-weight: bold;
  font-size: 0.95rem;
  text-transform: uppercase;
  padding-top: 0.2rem;
}

.timeline-content {
  flex: 1;
  
  h3 {
    margin: 0 0 0.5rem 0;
    color: $color-heading;
    font-size: 1.3rem;
  }
  
  h4 {
    margin: 0 0 1rem 0;
    color: rgba($color-body, 0.8);
    font-size: 0.9rem;
    font-weight: normal;
  }
  
  ul {
    margin: 0;
    padding-left: 1.2rem;
    
    li {
      color: rgba($color-body, 0.9);
      font-size: 0.95rem;
      line-height: 1.5;
      margin-bottom: 0.5rem;
      
      &:last-child {
        margin-bottom: 0;
      }
    }
  }
}
</style>
