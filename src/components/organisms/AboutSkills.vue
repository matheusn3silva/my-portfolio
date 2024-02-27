<template>
  <section class="skills">
    <div class="front">
      <h3 class="title__skill">Front-End</h3>
      <div class="icons__skills">
        <div class="icon">
          <img src="../../assets/images/icons/html-icon.svg" alt="html icon" />
        </div>
        <div class="icon">
          <img src="../../assets/images/icons/css-icon.svg" alt="css icon" />
        </div>
        <div class="icon">
          <img
            src="../../assets/images/icons/js-icon.svg"
            alt="javascript icon"
          />
        </div>
        <div class="icon">
          <img src="../../assets/images/icons/vue-icon.svg" alt="vue icon" />
        </div>
        <div class="icon">
          <img
            src="../../assets/images/icons/ts-icon.svg"
            alt="typescript icon"
          />
        </div>
        <div class="icon">
          <img src="../../assets/images/icons/sass-icon.svg" alt="sass icon" />
        </div>
        <div class="icon">
          <img
            src="../../assets/images/icons/tailwind-icon.svg"
            alt="tailwind icon"
          />
        </div>
      </div>
    </div>
    <div class="back">
      <h3 class="title__skill">Back-End</h3>
      <div class="icons__skills">
        <div class="icon">
          <img src="../../assets/images/icons/node-icon.svg" alt="Node" />
        </div>
        <div class="icon">
          <img src="../../assets/images/icons/adonis-icon.svg" alt="Adonis" />
        </div>
      </div>
    </div>
    <div class="tools">
      <h3 class="title__skill">Ferramentas</h3>
      <div class="icons__skills">
        <div class="icon">
          <img
            src="../../assets/images/icons/figma-icon.svg"
            alt="figma icon"
          />
        </div>
        <div class="icon">
          <img src="../../assets/images/icons/git-icon.svg" alt="git icon" />
        </div>
        <div class="icon">
          <img
            src="../../assets/images/icons/docker-icon.svg"
            alt="docker icon"
          />
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({})
</script>

<style scoped>
.skills {
  width: 100%;
  height: 100%;
  padding: 10rem 3rem;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1rem;
}

.front,
.back,
.tools {
  width: 100%;
  padding: 3rem 0;
  border: 1px solid var(--dark-gray);
  background-color: var(--dark);
  box-shadow:
    rgba(0, 0, 0, 0.25) 0px 54px 55px,
    rgba(0, 0, 0, 0.12) 0px -12px 30px,
    rgba(0, 0, 0, 0.12) 0px 4px 6px,
    rgba(0, 0, 0, 0.17) 0px 12px 13px,
    rgba(0, 0, 0, 0.09) 0px -3px 5px;
  transition: border-color 0.3s;
}

.front:hover,
.back:hover,
.tools:hover {
  border-color: var(--brand);
}

.title__skill {
  margin-bottom: 3rem;
  font-size: 2rem;
  text-align: center;
  text-transform: uppercase;
}

.icons__skills {
  width: 100%;
  padding: 0 2.8rem;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-auto-rows: 1fr;
  gap: 1rem;
  justify-items: center;
}

.icons__skills .icon {
  width: 10rem;
  height: 10rem;
  padding: 1rem;
  display: flex;
  justify-content: center;
  align-items: center;
  border: 1px solid var(--dark-gray);
  border-radius: 0.5rem;
  cursor: pointer;
  transition: border-color 0.3s;
}

.icons__skills .icon:hover {
  border-color: var(--white);
}

@media screen and (max-width: 1080px) {
  .skills {
    grid: auto / 1fr 1fr;
  }
}

@media screen and (max-width: 780px) {
  .skills {
    grid: 1fr 1fr 1fr / 1fr;
  }

  .front,
  .back,
  .tools {
    box-shadow: none;
  }
  .title__skill {
    margin: 2rem 0 6rem;
  }
}

@media screen and (max-width: 480px) {
  .icons__skills {
    grid: auto / 1fr 1fr;
  }
}
</style>
