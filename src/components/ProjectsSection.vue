

<template>
  <div class="projects-section">
    <div class="container">
      <h2 class="section-title">Proyectos</h2>
      
      <div class="projects-grid">
        <!-- Project 1 -->
        <div class="project-card">
          <div class="project-header">
            <h3>Dashboard: Brecha Digital Móvil</h3>
            <span class="year">2026</span>
          </div>
          <p class="tech">Streamlit, scipy, statsmodels, Folium, Plotly</p>
          <p class="desc">
            Análisis estadístico (chi-cuadrado, Kruskal-Wallis, regresión) de cobertura móvil por región, zona y operadora con datos de OSIPTEL; mapa de calor interactivo e identificación de factores asociados a la brecha digital.
          </p>
          <a href="https://brecha-digital-peru.streamlit.app/" target="_blank" rel="noopener noreferrer" class="btn-demo">Ver Demo</a>
        </div>
        
        <!-- Project 2 -->
        <div class="project-card">
          <div class="project-header">
            <h3>Diagnóstico Respiratorio con Naive Bayes</h3>
            <span class="year">2025</span>
          </div>
          <p class="tech">Streamlit, scikit-learn, Plotly, pandas</p>
          <p class="desc">
            Clasificador probabilístico (Naive Bayes gaussiano y categórico) para predecir afecciones respiratorias a partir de signos vitales; visualización de matriz de confusión y métricas de clasificación.
          </p>
          <a href="https://redes-bayesinas-afecciones-respiratorias.streamlit.app/" target="_blank" rel="noopener noreferrer" class="btn-demo">Ver Demo</a>
        </div>
        
        <!-- Project 3 -->
        <div class="project-card">
          <div class="project-header">
            <h3>Análisis Espacial Bayesiano (Agricultura)</h3>
            <span class="year">2024</span>
          </div>
          <p class="tech">R, INLA, QGIS</p>
          <p class="desc">
            Modelado jerárquico bayesiano (modelos CAR) de vulnerabilidad climática en el sur del Perú; detección de autocorrelación espacial con índice de Moran — <strong>publicado en Springer</strong>.
          </p>
          <a href="https://link.springer.com/chapter/10.1007/978-3-032-20151-5_4" target="_blank" rel="noopener noreferrer" class="btn-demo">Publicación</a>
        </div>

        <!-- Project 4 -->
        <div class="project-card">
          <div class="project-header">
            <h3>Chatbot RAG con Panel Administrativo</h3>
            <span class="year">2025</span>
          </div>
          <p class="tech">FastAPI, PostgreSQL, LangChain, Vue.js, Django</p>
          <p class="desc">
            Chatbot institucional con arquitectura RAG (FAISS + LangChain) y panel en Vue.js para gestión de usuarios, categorías, base de conocimiento y monitoreo; backend en Django.
          </p>
        </div>

        <!-- Project 5 -->
        <div class="project-card">
          <div class="project-header">
            <h3>Repositorio Institucional IIDEAA</h3>
            <span class="year">2025</span>
          </div>
          <p class="tech">React, SCSS, Three.js, PWA, Django</p>
          <p class="desc">
            Repositorio de publicaciones científicas del Instituto de Investigación y Desarrollo Andino Amazónico; frontend responsive con React y backend con Django REST framework.
          </p>
          <a href="https://iideaa.unap.edu.pe/inicio" target="_blank" rel="noopener noreferrer" class="btn-demo">Ver Demo</a>
        </div>

        <!-- Project 6 -->
        <div class="project-card">
          <div class="project-header">
            <h3>Dashboard: Análisis Agrícola Agropuno</h3>
            <span class="year">2024</span>
          </div>
          <p class="tech">R, Shiny, Plotly, dplyr, ggplot2</p>
          <p class="desc">
            Aplicación interactiva para el análisis de siembra y producción agrícola en las 13 provincias de Puno (1997--2021); evaluación estadística automática con pruebas de hipótesis.
          </p>
          <a href="https://ajmaquera.shinyapps.io/Agropuno/" target="_blank" rel="noopener noreferrer" class="btn-demo">Ver Demo</a>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use '../styles/variables.scss' as *;

.projects-section {
  width: 100%;
  padding: 4rem 2rem;
  box-sizing: border-box;
  background-color: rgba(0, 0, 0, 0.03);
}

.container {
  max-width: 1600px;
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

.projects-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2rem;
  
  @media (max-width: 1200px) {
    grid-template-columns: repeat(2, 1fr);
  }
  
  @media (max-width: 768px) {
    grid-template-columns: 1fr;
  }
}

.project-card {
  background: rgba($color-surface-light, 0.9);
  border: 1px solid rgba($color-accent, 0.3);
  /* RECTO */
  border-radius: 0;
  padding: 1.5rem;
  display: flex;
  flex-direction: column;
  transition: transform 0.3s ease, border-color 0.3s ease;
  
  &:hover {
    transform: translateY(-5px);
    border-color: $color-accent;
    background: rgba($color-surface-light, 1);
  }
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.5rem;
  
  h3 {
    margin: 0;
    color: $color-heading;
    font-size: 1.2rem;
    line-height: 1.3;
  }
  
  .year {
    color: $color-accent-2;
    font-size: 0.85rem;
    font-weight: bold;
    margin-left: 1rem;
  }
}

.tech {
  color: $color-accent;
  font-size: 0.85rem;
  font-weight: 600;
  margin: 0 0 1rem 0;
}

.desc {
  color: rgba($color-body, 0.9);
  font-size: 0.95rem;
  line-height: 1.5;
  margin-bottom: 1.5rem;
  flex: 1; /* Pushes button to bottom */
}

.btn-demo {
  display: inline-block;
  align-self: flex-start;
  padding: 0.5rem 1.2rem;
  background: transparent;
  color: $color-accent-2;
  text-decoration: none;
  font-weight: bold;
  font-size: 0.9rem;
  text-transform: uppercase;
  border: 1px solid $color-accent-2;
  /* RECTO */
  border-radius: 0;
  transition: background 0.3s ease, color 0.3s ease;
  
  &:hover {
    background: $color-accent-2;
    color: $color-bg-dark;
  }
}
</style>
