<template>
  <div class="index-content">
    <div class="index-hero container">
      <AppHello />
      <AppTerminal />
    </div>
    <!-- <hr>
    <section class="container">
      <h2>Últimos posts</h2>
      <div class="posts">
        <div v-for="(n,index)  in 3" :key="index" class="article-item"> 
          <nuxt-link to="/">
            <div class="card">
              <div class="card-image">
                <img src="https://cdn-aphna.nitrocdn.com/OFXwiHGWaekcBHFstRKBhwlYKJsfmLsh/assets/static/optimized/rev-1663ecc/wp-content/uploads/fondo-de-programacion-web_ok.jpg" />
              </div>
              <div class="card-content">
                <div class="card-title">
                  ¿La programación es para todos?
                </div>
                <div class="cord-body">
                  Neque porro quisquam est qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit...
                </div>
              </div>
            </div>
          </nuxt-link>
        </div>
      </div>
    </section>
        <section class="container">
        <AppQuote />
    </section> -->
  </div> 

</template>

<script>

export default {
 head() {
    return{
      title: 'Hola | Cristhian Mesta',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Hola, Soy Cristhian Mesta'
        }
      ],
    }
  }
}
</script>

<style lang="scss" scoped>

@import '/assets/css/utilities/_variables';

.index-content{
  display: flex;
  flex-flow: column nowrap;
  
}

.index-hero{
  display: flex;
  gap: 1rem;
  flex-direction: column;
  align-items: center;
  margin: 3rem auto;


  @media (min-width: $breakpoint-extrawidescreen) {
    flex-direction: row;
  }
}


.posts{
    margin-top: 1rem;
    margin-bottom: 1rem;
    display: grid;
    gap: 1.5rem;

    grid-template-columns: repeat(1, 1fr);

     @media (min-width: $breakpoint-widescreen){
        grid-template-columns: repeat(3, 1fr);
    }

     @media (min-width: $breakpoint-extrawidescreen){
        grid-template-columns: repeat(3, 1fr);
    }
}




</style>