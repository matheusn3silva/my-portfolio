<template>
  <header class="header-light">
    <div class="logo">MatheusNDS</div>
    <nav>
      <ul>
        <li @click="changePage('Home')">Início</li>
        <li @click="changePage('About')">Sobre Mim</li>
        <li @click="changePage('Project')">Projetos</li>
      </ul>
    </nav>
  </header>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  methods: {
    changePage(page: string) {
      this.$emit('changePage', page)
    }
  }
})
</script>

<style scoped>
header {
  height: 60px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 5rem;
  font-size: 1.6rem;
  font-weight: 500;
  background-color: var(--dark-gray);
}

nav ul {
  display: flex;
  align-items: center;
  list-style: none;
  gap: 4rem;
}

nav ul li {
  cursor: pointer;
  transition: color 0.5s;
}

nav ul li:hover {
  color: var(--brand);
}

@media screen and (max-width: 780px) {
  header {
    justify-content: center;
    font-size: 1.8rem;
  }
  header .logo {
    display: none;
  }
}

@media screen and (max-width: 480px) {
  header {
    justify-content: center;
    font-size: 1.4rem;
  }
  header .logo {
    display: none;
  }
}
</style>
