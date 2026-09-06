<template>
  <div class="hero-section">
    <div class="hero-content">
      <div class="profile-photo">
        <img src="/good.png" alt="Aldair Maquera" />
      </div>
      
      <h1 class="hero-title">Aldair Maquera</h1>
      
      <div class="content">
        <div class="content__container">
          <p class="content__container__text">Soy</p>
          <ul class="content__container__list">
            <li class="content__container__list__item">Analista de Datos !</li>
            <li class="content__container__list__item">Desarrollador Web !</li>
            <li class="content__container__list__item">Ing. Estadístico !</li>
            <li class="content__container__list__item">Backend Dev !</li>
          </ul>
        </div>
      </div>

      <div class="social-links">
        <a href="mailto:harperafterhours@gmail.com" target="_blank" rel="noopener noreferrer">
          <img src="https://img.shields.io/badge/-Email-1B3A5C?style=flat-square&logo=gmail&logoColor=white" alt="Email" />
        </a>
        <a href="https://github.com/ajmaquera" target="_blank" rel="noopener noreferrer">
          <img src="https://img.shields.io/badge/-GitHub-1B3A5C?style=flat-square&logo=github&logoColor=white" alt="GitHub" />
        </a>
        <a href="https://gitlab.com/ajmaquera" target="_blank" rel="noopener noreferrer">
          <img src="https://img.shields.io/badge/-GitLab-1B3A5C?style=flat-square&logo=gitlab&logoColor=white" alt="GitLab" />
        </a>
        <a href="https://stackoverflow.com/users/32708576/aldair-maquera" target="_blank" rel="noopener noreferrer">
          <img src="https://img.shields.io/badge/-StackOverflow-1B3A5C?style=flat-square&logo=stackoverflow&logoColor=white" alt="StackOverflow" />
        </a>
        <a href="https://x.com/ajmaquera" target="_blank" rel="noopener noreferrer">
          <img src="https://img.shields.io/badge/-X-1B3A5C?style=flat-square&logo=x&logoColor=white" alt="X" />
        </a>
        <a href="https://pe.linkedin.com/in/aldair-maquera-andrade/" target="_blank" rel="noopener noreferrer">
          <img src="https://img.shields.io/badge/-LinkedIn-1B3A5C?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn" />
        </a>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use '../styles/variables.scss' as *;

.hero-section {
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: transparent;
}

.hero-content {
  text-align: center;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1.5rem;
}

.profile-photo {
  width: 180px;
  height: 180px;
  border: 4px solid $color-accent;
  padding: 5px;
  background: rgba($color-accent, 0.1);
  /* RECTO: NO border-radius */
  
  img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    display: block;
  }
}

.hero-title {
  font-size: 3rem;
  margin: 0;
  color: $color-heading;
  text-transform: uppercase;
  letter-spacing: 2px;
}

/* User provided CSS Animation */
.content {
  position: relative;
  height: 60px;
  overflow: hidden;
  font-family: 'Lato', sans-serif;
  font-size: 35px;
  line-height: 40px;
  color: $color-body;
  display: flex;
  justify-content: center;
  
  &__container {
    font-weight: 600;
    overflow: hidden;
    height: 40px;
    padding: 0 40px;
    position: relative;
    display: flex;
    align-items: flex-start;

    &:before {
      content: '[';
      left: 0;
    }

    &:after {
      content: ']';
      position: absolute;
      right: 0;
    }

    &:after, &:before {
      position: absolute;
      top: 0;
      color: $color-accent;
      font-size: 42px;
      line-height: 40px;
      animation-name: opacity;
      animation-duration: 2s;
      animation-iteration-count: infinite;
    }

    &__text {
      display: inline;
      margin: 0;
      margin-right: 15px;
    }

    &__list {
      margin-top: 0;
      padding-left: 0;
      text-align: left;
      list-style: none;
      animation-name: change;
      animation-duration: 10s;
      animation-iteration-count: infinite;

      &__item {
        line-height: 40px;
        margin: 0;
        white-space: nowrap;
      }
    }
  }
}

@keyframes opacity {
  0%, 100% {opacity:0;}
  50% {opacity:1;}
}

@keyframes change {
  0%, 12.66%, 100% {transform:translate3d(0,0,0);}
  16.66%, 29.32% {transform:translate3d(0,-25%,0);}
  33.32%,45.98% {transform:translate3d(0,-50%,0);}
  49.98%,62.64% {transform:translate3d(0,-75%,0);}
  66.64%,79.3% {transform:translate3d(0,-50%,0);}
  83.3%,95.96% {transform:translate3d(0,-25%,0);}
}

.social-links {
  display: flex;
  gap: 1rem;
  margin-top: 1rem;
  
  a {
    transition: transform 0.2s ease;
    display: block;
    &:hover {
      transform: translateY(-3px);
    }
    
    img {
      height: 28px;
    }
  }
}
</style>
