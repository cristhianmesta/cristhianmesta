<template>
  <div class="tecnology">
      <h2 class="tecnology-title">
            Tecnologías
      </h2>
      <div class="tecnology-body">
        <div v-for="(tecnology, index) in tecnologies" :key="index"
             class="tecnology-item">
          <div class="tecnology-item-title">
            {{ tecnology.section }}:
          </div>
          <div class="tecnology-item-body">
            <figure v-for="lan in tecnology.items" :key="lan.image.replace(' ','')"> 
              <img :src="require(`~/assets/img/tecnologies/${lan.image}`)" height="48" :alt="lan.name" /> 
              <figcaption>{{ lan.name }}</figcaption>
            </figure>
          </div>
        </div>
      </div>
  </div>
</template>

<script>
export default {
    name: 'Tecnologies',
    props: {
        tecnologies: {
            type: Array,
            default: () => []
        },
    },
}
</script>

<style lang="scss" scoped>

@import '/assets/css/utilities/_variables';

.tecnology{

  .tecnology-title{
    margin-bottom: 1rem;
    display: inline-block;
    border-bottom: 4px solid rgb(167, 167, 167);
    color: $color-text-strong;
  }

  .tecnology-body{

    .tecnology-item{
      padding: 1rem;
      margin-bottom: 1rem;
      background-color: #fafafa;
      border: 1px solid #f1f0f0;
      border-radius: 10px;

      .tecnology-item-title{
        font-size: 1.2rem;
        color: rgb(167, 167, 167);
        font-weight: 500;
        margin-bottom: .5rem;
      }

      .tecnology-item-body{
        margin-top: .75rem;
        margin-bottom: .75rem;
        padding-top: 1rem;
        display: flex;
        flex-wrap: wrap;
        gap: .75rem;
        text-align: center;
        font-size: 0.8rem;
      }
    }
  }
}

</style>7