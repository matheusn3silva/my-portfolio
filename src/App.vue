<template>
  <HeaderV @changePage="valuePage" />
  <component :is="currentPage" />
  <FooterV />
</template>

<script lang="ts">
import { defineComponent } from 'vue'

import HeaderV from './components/organisms/Header.vue'
import FooterV from './components/organisms/Footer.vue'
import Home from './pages/Home.vue'
import About from './pages/About.vue'
import Project from './pages/Project.vue'

export default defineComponent({
  components: { HeaderV, FooterV, Home, About, Project },
  data() {
    return {
      currentPage: 'Home'
    }
  },
  methods: {
    valuePage(value: string) {
      this.currentPage = value
    }
  }
})
</script>
