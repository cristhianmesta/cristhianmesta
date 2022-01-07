<template>
  <article class="blog container">
    <section class="hero">
      <h1>
        Blog
      </h1>
      <p>Notas de programación para todos.</p>
    </section>
      
  </article>
</template>

<script>
export default {
 head() {
    return{
      title: 'Blog | Cristhian Mesta',
      meta: [
          {
            hid: 'description',
            name: 'description',
            content: 'Blog para programadores y no programadores.'
          }
        ],
    }
 }
}
</script>

<style lang="scss" scoped>

@import '/assets/css/utilities/_variables';


.blog{

  .blog-hero{
    font-family: $font-title;

    h1{
        font-size: 3rem;
    }
  }
}



</style>