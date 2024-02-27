<template>
  <img src="path" alt="" />
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue'

export default defineComponent({
  props: {
    path: { type: String, required: true }
  },
  setup(props) {
    const imagePath = ref('');

    // Carrega a imagem de forma assíncrona
    import(props.path)
      .then((module) => {
        imagePath.value = module.default;
      })
      .catch((error) => {
        console.error('Erro ao carregar imagem:', error);
      });

    return { imagePath };
  }
})
</script>

<style scoped>

</style>