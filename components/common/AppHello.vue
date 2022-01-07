<template>
    <div class="hello">
        <div class="hello-icon">👋</div>
        <h1>
            Hola, <br>
            Soy <span><nuxt-link to="sobre-mi" class="link-blue">Cristhian Mesta</nuxt-link></span>
        </h1>
        <p> 
          Ingeniero, desarrollador de software, lector, a veces dibujante, y ahora creo contenido para la web.
        </p>
        <br>
        <div class="hello-follow">
          <AppTwitterButton />
          <AppGitHubButton />
        </div>
    </div>
</template>

<script>
export default {
    name: 'AppHello'
}
</script>

<style lang="scss" scoped>

@import '/assets/css/utilities/_variables';

.hello{
  padding-left: 0;
  margin-top: 0;
  margin-bottom: 5rem;
  flex-grow: 1;

  @media (min-width: $breakpoint-extrawidescreen) {
    margin-top: 3rem;
    margin-bottom: 3rem;
    padding-right: 3rem ;
  }

  .hello-icon{
    font-size: 2rem;
    
    @media (min-width: $breakpoint-extrawidescreen) {
      font-size: 3rem;
    }
  }

  h1{
    font-size: 2rem;
    margin-top: 1.2rem;
    margin-bottom: 1.2rem;
    font-family: $font-title;

    @media (min-width: $breakpoint-extrawidescreen) {
      font-size: 2.2rem;
    }
  }

  p{
    font-size: 1.6rem;
    line-height: 2.8rem;

    @media (min-width: $breakpoint-extrawidescreen) {
      font-size: 1.8rem;
    }
  }

  .hello-follow{
      font-size: 1rem;
  }

}

</style>