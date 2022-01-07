<template>
  <article class="container">
    <section class="hero">
      <h1>
        Contacto
      </h1>
      <p>Si te gustó el contenido de mi sitio, necesitas algo de ayuda o quizá tienes una recomendación que me pueda ayudar, me puedes escribir a 
        mi <a class="link-email" href="mailto:cristhianmesta@hotmail.com">correo electrónico</a> 📧.
      </p>
      <br>
      <p>Además, te invito a que me sigas o me contactes por mis redes:</p>
      
      <p class="redes">
        <a class="link-github" href="https://github.com/cristhianmesta" target="_blank">
           GitHub
        </a>
        , 
        <a class="link-linkedin" href="https://www.linkedin.com/in/cristhianmesta" target="_blank">
          LinkedIn
        </a>
         y 
        <a class="link-twitter" href="https://twitter.com/cristhianmesta" target="_blank">
          Twitter
        </a>
      </p>
    </section>
      
  </article>
</template>

<script>
export default {
 head() {
    return{
        title: 'Contáctame | Cristhian Mesta',
        meta: [
            {
                hid: 'description',
                name: 'description',
                content: 'Desde aqui puedes contactarme.'
            }
        ],
    }
  },
}
</script>