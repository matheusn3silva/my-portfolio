<template>
  <section class="project">
    <ProjectTemplate />
  </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import ProjectTemplate from '../components/templates/ProjectTemplate.vue'

export default defineComponent({
  components: { ProjectTemplate }
})
</script>

<style scoped>

</style>