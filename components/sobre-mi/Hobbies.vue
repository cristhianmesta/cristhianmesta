<template>
  <div class="hobbies">
      <h2 class="hobbies-title">
          Intereses
      </h2>
      <div class="hobbies-body">
        <ul>
          <li v-for="(hobbie, index) of hobbies" :key="`hobbie${index}`">
            {{ hobbie }}
          </li>
        </ul>
      </div>
  </div>
</template>

<script>
export default {
    name: 'Hobbies',
    props: {
        hobbies: {
            type: Array,
            default: () => []
        },
    }
}
</script>

<style lang="scss" scoped>

@import '/assets/css/utilities/_variables';

.hobbies{

  .hobbies-title{
    margin-bottom: 1rem;
    display: inline-block;
    border-bottom: 4px solid rgb(179, 248, 100);
  }

  .hobbies-body{
    ul{
      list-style: none;
      padding-left: 1rem;

      li{
        font-size: 1.1rem;
        margin-bottom: .5rem;
      }
    }
  }
}

</style>