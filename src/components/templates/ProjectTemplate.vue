<template>
  <section class="project__template">
    <h2>PROJE<span>TOS</span></h2>
    <CardProject
      title="SPACE TOURISM"
      deploy="https://space-tourism-phi-five.vercel.app/"
      github="https://github.com/matheusn3silva/space_tourism?tab=readme-ov-file"
      text="Já viajou para o espaço? Não?? Aqui eu te mostro como seria uma viagem para o espaço com uma equipe muito bem treinada e com 4 destinos diferentes possíveis."
      tag1="Vue.js"
      tag2="Typescript"
      tag3="Sass"
      :reverse="false"
    >
      <img src="../../assets/images/projects/space-tourism.jpg" alt="" />
    </CardProject>
    <CardProject
      title="MARCOS PORTFOLIO"
      deploy="https://marcos-portfolio-two.vercel.app/"
      github="https://github.com/matheusn3silva/marcos-portfolio"
      text="Portfólio do Marcos, apresenta seus serviços e sua personalidade com um lindo visual light e links para você entrar em contanto direto com ele."
      tag1="Vue.js"
      tag2="Typescript"
      tag3="CSS3"
      :reverse="true"
    >
      <img
        src="../../assets/images/projects/marcos-portfolio.jpg"
        alt="Marcos portfolio imagem"
      />
    </CardProject>
    <CardProject
      title="TODO LIST"
      deploy="https://todo-list-one-sable.vercel.app/"
      github="https://github.com/matheusn3silva/todo-list"
      text="Faça sua lista de tarefas aqui. Crie tarefas que podem ser conclúidas ou não e exclua as que você não quiser mais. É possível escolher entre tema light ou dark."
      tag1="HTML5"
      tag2="CSS3"
      tag3="Javascript"
      :reverse="false"
    >
      <img
        src="../../assets/images/projects/todo-list.jpg"
        alt="Todo list project image"
      />
    </CardProject>
    <CardProject
      title="SHOP JORDAN SHOES"
      deploy="https://shop-jordan-shoes.vercel.app/"
      github="https://github.com/matheusn3silva/shop-j-shoes"
      text="Uma loja virtual online que apresenta diferentes tipos de tênis Jordan, para que o cliente possa visualizar cada um e ver seu preço de forma intuitiva e fácil."
      tag1="HTML5"
      tag2="Sass"
      tag3="Javascript"
      :reverse="true"
    >
      <img
        src="../../assets/images/projects/shop-shoes.jpg"
        alt="Shop Jordan Shoes project image"
      />
    </CardProject>
  </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import CardProject from '../molecules/CardProject.vue'

export default defineComponent({
  components: { CardProject }
})
</script>

<style scoped>
.project__template {
  width: 100%;
  height: 100%;
  padding: 0 5rem;
}
.project__template h2 {
  margin: 7rem 0 7rem;
  font-size: 4rem;
  text-align: center;
  font-weight: 600;
}

.project__template h2 span {
  color: var(--brand);
}

img {
  width: 100%;
}

@media screen and (max-width: 480px) {
  .project__template {
    padding: 0 2rem;
  }
}
</style>
