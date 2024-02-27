<template>
  <section class="home-template">
    <Apresentation />
  </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import Apresentation from '../molecules/Apresentation.vue'

export default defineComponent({
  components: { Apresentation }
})
</script>

<style scoped>
.home-template {
  width: 100%;
  height: 100vh;
  margin: 10rem 0;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
