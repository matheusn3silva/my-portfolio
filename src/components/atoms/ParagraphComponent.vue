<template>
  <p>{{ value }}</p>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  props: {
    value: {
      type: String,
      required: true
    }
  }
})
</script>

<style scoped>
p {
  font-size: 1.6rem;
  line-height: 1.8;
  margin-bottom: 2rem;
}

@media screen and (max-width: 480px) {
  p {
    font-size: 1.4rem;
    text-align: center;
  }
}
</style>
