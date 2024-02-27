<template>
  <section class="about__template">
    <h2>SOBRE <span>MIM</span></h2>
    <AboutDescription />
    <h2>MEUS OBJ<span>ETIVOS</span></h2>
    <AboutServices />
    <h2>HABIL<span>IDADES</span></h2>
    <AboutSkills />
    <section class="goals"></section>
  </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import AboutDescription from '../organisms/AboutDescription.vue'
import AboutSkills from '../organisms/AboutSkills.vue'
import AboutServices from '../organisms/AboutGoals.vue'

export default defineComponent({
  components: { AboutDescription, AboutSkills, AboutServices }
})
</script>

<style scoped>
.about__template {
  width: 100%;
  height: 100%;
}

.about__template h2 {
  margin: 8rem 0 2rem;
  font-size: 4rem;
  text-align: center;
  font-weight: 600;
}

.about__template h2 span {
  color: var(--brand);
}

@media screen and (max-width: 480px) {
  .about__template h2 {
    font-size: 3rem;
    margin: 6rem 0 0rem;
  }
}
</style>
