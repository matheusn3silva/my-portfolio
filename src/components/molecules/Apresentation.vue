<template>
  <section class="apresentation">
    <h1>DESENVOLVEDOR <span>FRONT END</span></h1>
    <p>
      Criando e moldando o futuro com habilidades de Design e Desenvolvimento
      Frontend.
    </p>
    <a href="https://www.linkedin.com/in/matheusnsilva" target="_blank">
      Conheça-me
    </a>
    <div class="skills">
      <div class="icon html">
        <img src="../../assets/images/icons/html-icon.svg" alt="Html icon" />
      </div>
      <div class="icon css">
        <img src="../../assets/images/icons/css-icon.svg" alt="Css icon" />
      </div>
      <div class="icon js">
        <img
          src="../../assets/images/icons/js-icon.svg"
          alt="Javascript icon"
        />
      </div>
      <div class="icon vue">
        <img src="../../assets/images/icons/vue-icon.svg" alt="Vue js icon" />
      </div>
      <div class="icon nuxt">
        <img src="../../assets/images/icons/nuxt-icon.svg" alt="Nuxt js icon" />
      </div>
      <div class="icon ts">
        <img
          src="../../assets/images/icons/ts-icon.svg"
          alt="Typescript icon"
        />
      </div>
      <div class="icon sass">
        <img src="../../assets/images/icons/sass-icon.svg" alt="Sass icon" />
      </div>
      <div class="icon tailwind">
        <img
          src="../../assets/images/icons/tailwind-icon.svg"
          alt="Tailwind icon"
        />
      </div>
    </div>
  </section>
</template>

<style scoped>
.apresentation {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 6.2rem;
}

.apresentation h1 {
  font-size: 4.8rem;
  font-weight: 600;
  letter-spacing: 6%;
}

.apresentation h1 span {
  color: var(--brand);
}

.apresentation p {
  max-width: 550px;
  text-align: center;
  font-size: 1.8rem;
  letter-spacing: 4%;
}

.apresentation p,
.apresentation h1 {
  text-shadow: 0 2.5px 2.5px #000000cc;
}

.apresentation a {
  max-width: 27rem;
  width: 100%;
  padding: 1.8rem 0;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.8rem;
  text-decoration: none;
  color: var(--white);
  background-color: var(--brand);
  border: none;
  border-radius: 1px;
  cursor: pointer;
  transition: background-color 0.5s;
}

.apresentation a:hover {
  background-color: var(--btn-hover);
}

.apresentation .skills {
  display: flex;
  gap: 6rem;
}

.apresentation .skills .icon {
  width: 8rem;
  height: 8rem;
  padding: 1.6rem;
  display: flex;
  justify-content: center;
  align-items: center;
  border: 1px solid var(--dark-gray);
  border-radius: 0.5rem;
  cursor: pointer;
  transition: border-color 0.5s;
}

.apresentation .skills .icon img {
  width: 100%;
}

.apresentation .skills .icon.html:hover {
  border-color: #e44d26;
}

.apresentation .skills .icon.css:hover {
  border-color: #2962f0;
}

.apresentation .skills .icon.js:hover {
  border-color: #f7df1e;
}

.apresentation .skills .icon.vue:hover {
  border-color: #41b883;
}

.apresentation .skills .icon.nuxt:hover {
  border-color: #00838F;
}

.apresentation .skills .icon.ts:hover {
  border-color: #3178c6;
}

.apresentation .skills .icon.sass:hover {
  border-color: #cd6799;
}
.apresentation .skills .icon.tailwind:hover {
  border-color: #00b3d2;
}

@media screen and (max-width: 780px) {
  .apresentation h1 {
    font-size: 3.6rem;
  }

  .apresentation p {
    max-width: 38rem;
    font-size: 1.4rem;
  }

  .apresentation a {
    max-width: 20rem;
    padding: 1.4rem 0;
    font-size: 1.6rem;
  }

  .apresentation .skills {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-auto-rows: 50px;
    gap: 4rem;
  }
}

@media screen and (max-width: 480px) {
  .apresentation h1 {
    max-width: 30rem;
    font-size: 3rem;
    text-align: center;
  }

  .apresentation p {
    max-width: 28rem;
    font-size: 1.2rem;
  }

  .apresentation a {
    max-width: 16rem;
    padding: 1rem 0;
    font-size: 1.2rem;
  }

  .apresentation .skills {
    display: grid;
    grid: auto / repeat(3, 1fr);
    gap: 1rem;
  }
}
</style>
