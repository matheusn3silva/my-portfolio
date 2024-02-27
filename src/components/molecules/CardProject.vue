<template>
  <div :class="['card__project', { card__reverse: reverse === true }]">
    <div class="img">
      <slot />
    </div>
    <div class="project__description">
      <div>
        <h4>{{ title }}</h4>
        <a class="link__project" :href="deploy" target="_blank">Deploy</a>
        <a class="link__project" :href="github" target="_blank">Repositório</a>
        <ParagraphComponent class="paragraph" :value="text" />
      </div>
      <div class="tags">
        <span class="tag">{{ tag1 }}</span>
        <span class="tag">{{ tag2 }}</span>
        <span class="tag">{{ tag3 }}</span>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import ParagraphComponent from '../atoms/ParagraphComponent.vue'

export default defineComponent({
  components: { ParagraphComponent },
  props: {
    title: { type: String, required: true },
    deploy: { type: String, required: true },
    github: { type: String, required: true },
    text: { type: String, required: true },
    tag1: { type: String, required: true },
    tag2: { type: String, required: true },
    tag3: { type: String, required: true },
    reverse: { type: Boolean, required: true }
  }
})
</script>

<style scoped>
.card__project {
  width: 100%;
  margin: 10rem 0;
  display: flex;
  justify-content: center;
  gap: 5rem;
  border: 1px solid var(--white);
  background-color: var(--dark-gray);
  padding: 3rem;
  border-radius: 1rem;
}

.card__reverse {
  flex-direction: row-reverse;
}
.card__project .img {
  width: 44rem;
  height: 29rem;
  display: flex;
  justify-content: center;
  align-items: center;
}

.card__project .project__description {
  display: flex;
  flex-direction: column;
  justify-content: space-around;
}

.card__project .project__description h4 {
  font-size: 2.8rem;
  font-weight: 500;
  text-transform: uppercase;
}

.card__project .project__description a.link__project {
  margin: 2rem 2rem 2rem 0;
  padding: 0.5rem 2rem;
  display: inline-block;
  border: 1px solid var(--brand);
  border-radius: 0.5rem;
  color: gray;
  font-size: 1.4rem;
  text-align: center;
  text-decoration: none;
  transition: color 0.3s;
}

.card__project .project__description a.link__project:hover {
  color: var(--white);
}

.card__project .project__description .paragraph {
  max-width: 70rem;
}

.card__project .project__description .tags .tag {
  display: inline-block;
  padding: 0.3rem 3rem;
  margin: 1rem 1rem 1rem 0;
  font-size: 1.6rem;
  font-weight: 400;
  border-radius: 2rem;
  border: 1px solid var(--brand);
}

@media screen and (max-width: 780px) {
  .card__project {
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  .card__project .img {
    max-width: 34rem;
  }
}

@media screen and (max-width: 480px) {
  .card__project {
    padding: 0 1.6rem 1rem 1.6rem;
  }

  .card__project .img {
    max-width: 24rem;
  }

  .card__project .project__description .paragraph {
    text-align: start;
  }
}
</style>
