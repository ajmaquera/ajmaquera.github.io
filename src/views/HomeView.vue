<script setup lang="ts">
import Init from '../components/init.vue'
import HeroSection from '../components/HeroSection.vue'
import AboutSection from '../components/AboutSection.vue'
import ExperienceSection from '../components/ExperienceSection.vue'
import ProjectsSection from '../components/ProjectsSection.vue'
</script>

<template>
  <Init>
    <div class="portfolio-container">
    <header class="main-header">
      <div class="logo">
        <router-link to="/hello">Dair Dev</router-link>
      </div>
      <nav class="main-nav">
        <a href="#hero">Inicio</a>
        <a href="#about">Sobre Mí</a>
        <a href="#experience">Experiencia</a>
        <a href="#projects">Proyectos</a>
      </nav>
    </header>

    <main class="scroll-container">
      <section id="hero" class="scroll-section">
        <HeroSection />
      </section>
      <section id="about" class="scroll-section">
        <AboutSection />
      </section>
      <section id="experience" class="scroll-section">
        <ExperienceSection />
      </section>
      <section id="projects" class="scroll-section">
        <ProjectsSection />
      </section>
    </main>
  </div>
  </Init>
</template>

<style lang="scss">
@use '../styles/variables.scss' as *;

body, html {
  margin: 0;
  padding: 0;
  min-height: 100%;
  background-color: $color-bg-light;
  background-image: radial-gradient(circle at 50% 50%, rgba($color-heading, 0.05) 0%, transparent 80%);
  background-attachment: fixed;
  color: $color-body;
  font-family: 'Lato', sans-serif;
}

.portfolio-container {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

.main-header {
  position: fixed;
  top: 0;
  width: 100%;
  height: 60px;
  background: rgba($color-bg-light, 0.9);
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 2rem;
  z-index: 1000;
  box-sizing: border-box;
  border-bottom: 1px solid rgba($color-heading, 0.1);

  .logo a {
    color: $color-heading;
    text-decoration: none;
    font-size: 1.5rem;
    font-weight: bold;
    text-transform: uppercase;
    letter-spacing: 2px;
  }

  .main-nav {
    display: flex;
    gap: 1.5rem;

    a {
      color: $color-body;
      text-decoration: none;
      font-size: 0.9rem;
      text-transform: uppercase;
      letter-spacing: 1px;
      transition: color 0.3s ease;

      &:hover {
        color: $color-accent;
      }
    }
  }
}

.scroll-container {
  flex: 1;
  scroll-behavior: smooth;
}

.scroll-section {
  min-height: 100vh;
  width: 100%;
  position: relative;
  display: flex;
  justify-content: center;
  align-items: flex-start;
  padding-top: 60px; /* Account for fixed header */
  box-sizing: border-box;
}

#hero {
  align-items: center;
}
</style>
