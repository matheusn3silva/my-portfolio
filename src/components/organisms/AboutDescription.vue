<template>
  <section class="about">
    <div class="img__container">
      <img src="@/assets/images/avatar.svg" alt="Meu avatar" />
    </div>
    <div class="description">
      <ParagraphComponent
        value="👋 Olá, sou Matheus Nascimento da Silva, um Programador Front-end
          focado em proporcionar a melhor experiência possível ao cliente. Minha
          abordagem envolve a criação de interfaces intuitivas e visualmente
          atraentes, sempre superando expectativas."
      />
      <ParagraphComponent
        value="Com habilidades técnicas atualizadas e uma mentalidade centrada no
          usuário, estou comprometido em utilizar as melhores tecnologias para
          garantir projetos de alta qualidade. Curto trabalhar de forma
          comunicativa, sempre interagindo com o cliente e pedindo feedback para
          que os projetos sejam os melhores possíveis."
      />
      <ParagraphComponent
        value="Estou pronto para enfrentar desafios e contribuir para o sucesso do
          seu próximo projeto, assegurando a excelência na experiência do
          usuário. Vamos criar algo incrível juntos!"
      />
    </div>
  </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import ParagraphComponent from '../atoms/ParagraphComponent.vue'

export default defineComponent({
  components: { ParagraphComponent }
})
</script>

<style scoped>
.about {
  width: 100%;
  height: 100%;
  padding: 5rem 3rem;
  display: grid;
  grid: 1fr / 1fr 1fr;
  justify-items: center;
  align-items: center;
}

.about .img__container {
  width: 80%;
  border-right: 1px solid var(--brand);
  padding-right: 3rem;
}

.about .img__container img {
  width: 100%;
}

.about .description {
  max-width: 600px;
}

@media screen and (max-width: 780px) {
  .about {
    grid: 1fr 1fr / 1fr;
  }

  .about .img__container {
    max-width: 500px;
    border-right: none;
    border-bottom: 1px solid var(--brand);
    padding: 0;
    padding-bottom: 2rem;
  }
}

@media screen and (max-width: 480px) {
  .about {
    padding: 0 2rem;
  }
}
</style>
