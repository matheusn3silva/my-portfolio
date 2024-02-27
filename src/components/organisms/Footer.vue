<template>
  <footer class="footer">
    <div class="contact">
      <a
        class="icon__contact"
        href="https://www.linkedin.com/in/matheusnsilva"
        target="_blank"
      >
        <i class="fa-brands fa-linkedin-in"></i>
      </a>
      <a
        class="icon__contact"
        href="https://www.github.com/matheusn3silva"
        target="_blank"
      >
        <i class="fa-brands fa-github"></i>
      </a>
      <a
        class="icon__contact"
        href="https://api.whatsapp.com/send?phone=5511978384169&text=Olá,%20como%20vai?!"
        target="_blank"
      >
        <i class="fa-brands fa-whatsapp"></i>
      </a>
      <a
        class="icon__contact"
        href="mailto:matheusnascimentox725@gmail.com"
        target="_blank"
      >
        <i class="fa-solid fa-envelope"></i>
      </a>
    </div>
    <a
      href="https://www.dropbox.com/scl/fi/qfpqqbpeyn4nk0p0sns06/Meu-curriculo.pdf?rlkey=0wpfrs76rskzkkkkmr3arxvan&dl=0"
      class="cv"
      target="_blank"
      >Veja meu CV</a
    >
    <div class="copyright">
      <p>© MATHEUS NASCIMENTO 2024 | Todos os direitos reservados</p>
    </div>
  </footer>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  setup() {
    return {}
  }
})
</script>

<style scoped>
.footer {
  width: 100%;
  height: 200px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 3rem;
  background-color: var(--dark-gray);
}

.footer .contact {
  display: flex;
  gap: 3rem;
}

.footer .contact .icon__contact {
  width: 5rem;
  height: 5rem;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 3rem;
  text-decoration: none;
  color: var(--white-gray);
  border-radius: 0.2rem;
  transition: background-color 0.5s;
}

.footer .contact .icon__contact:hover {
  background-color: var(--btn-hover);
}

.footer .cv {
  padding: 0.8rem 3rem;
  font-size: 1.6rem;
  text-decoration: none;
  border-radius: 3rem;
  background-color: var(--brand);
  color: var(--white);
  transition: background-color 0.5s;
}

.footer .cv:hover {
  background-color: var(--btn-hover);
}

.footer .copyright p {
  font-size: 1.2rem;
}

@media screen and (max-width: 480px) {
  .footer .contact .icon__contact {
    font-size: 2.4rem;
  }

  .footer .cv {
    padding: 0.4rem 2rem;
  }

  .footer .copyright p {
    font-size: 1rem;
  }
}
</style>
