<template>
  <article class="quete">
    <div class="quete-content">
      <p>
        Un comentario es un síntoma de no haber conseguido escribir un código claro.
      </p>
    </div>
    <footer class="quete-author">Robert C. Martin (Uncle Bob)</footer>
  </article>
</template>

<script>

export default {
  name: 'AppQuote',

}

</script>

<style lang="scss" scoped>

@import '/assets/css/utilities/_variables';

.quete{
  width: 90%;
  margin: 2rem auto;
  padding: 1rem 1rem;
  border: 4px solid rgb(200, 237, 252);
  border-radius: 10px;
  background-color: rgb(245, 251, 253);
  box-shadow: rgba(0, 0, 0, 0.25) 0px 25px 50px -12px;

  @media (min-width: $breakpoint-smallscreen) {
      width: 70%;
      margin: 3rem auto;
      padding: 1.5rem 1.5rem;
  }

  @media (min-width: $breakpoint-widescreen) {
      width: 60%;
      margin: 3rem auto;
  }

    @media (min-width: $breakpoint-extrawidescreen) {
      width: 50%;
      margin: 3rem auto;
  }
}

.quete-content{
  display: flex;
  font-size: 1.2rem;
  text-align: center;
  margin-bottom: 1rem;

  @media (min-width: $breakpoint-tablet) {
    font-size: 1.6rem;
  }

  p{
      padding-left: 1rem;
      padding-right: 1rem;
      color: $color-text-light;

      @media (min-width: $breakpoint-tablet) {
        padding-left: 1.5rem;
        padding-right: 1.5rem;
      }
  }

  &::before, &::after {
    font-family: 'Times New Roman', Times, serif;
    font-size: 4rem;
    margin: auto 0;
    color: rgb(31, 164, 216);

    @media (min-width: $breakpoint-tablet) {
      font-size: 5rem;
    }
  }

  &::before {
    content: "‟";
  }

  &::after {
    content: "”";
  }
}

.quete-author{
  text-align: center;
  font-size: .9rem;
  color: rgb(31, 164, 216);
  font-weight: bold;

  @media (min-width: $breakpoint-tablet) {
    font-size: 1.1rem;
  }
}

</style>