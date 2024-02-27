<template>
  <section class="goals">
    <div class="description">
      <ol>
        <li>
          <ParagraphComponent
            class="paragraph"
            value="Sou uma pessoa apaixonada pelo aprendizado contínuo e estou sempre buscando melhorar e perseguir meus sonhos. A programação é minha principal meta de carreira, onde constantemente busco aprimorar minhas habilidades e adquirir novos conhecimentos neste vasto universo. Estou determinado a buscar oportunidades para atuar nesta área, apesar dos desafios que possam surgir."
          />
        </li>
        <li>
          <ParagraphComponent
            class="paragraph"
            value="Além disso, tenho o sonho de poder viajar e trabalhar no exterior para enriquecer minha jornada pessoal e aprimorar os serviços que posso oferecer."
          />
        </li>
        <li>
          <ParagraphComponent
            class="paragraph"
            value="Tenho como um objetivo ambicioso, que pode ainda estar um pouco distante de ser realizado (ou não), o desejo de um dia empreender, criando minha própria empresa, serviços e definindo metas de realização."
          />
        </li>
      </ol>
    </div>
    <div class="img__container">
      <img src="@/assets/images/avatar-lendo.svg" alt="Meu avatar" />
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
.goals {
  width: 100%;
  height: 100%;
  padding: 5rem 4rem;
  display: grid;
  grid: 1fr / 1fr 1fr;
  justify-items: center;
  align-items: center;
}

.goals .img__container {
  width: 80%;
  border-left: 1px solid var(--brand);
  padding-left: 3rem;
}

.goals .img__container img {
  width: 100%;
}

.goals .description {
  max-width: 600px;
}

.goals .description ol {
  font-size: 1.8rem;
}

@media screen and (max-width: 780px) {
  .goals {
    grid: 1fr 1fr / 1fr;
  }

  .goals .img__container {
    max-width: 500px;
    border-left: none;
    border-top: 1px solid var(--brand);
    padding: 0;
    padding-top: 3rem;
  }
}

@media screen and (max-width: 480px) {
  .goals {
    padding: 5rem 2rem;
  }

  .goals .description ol {
    font-size: 1.4rem;
  }

  .goals .description {
    padding: 0 1rem;
  }
}
</style>
