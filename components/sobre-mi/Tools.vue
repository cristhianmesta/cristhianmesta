<template>
  <div class="tool">
      <h2 class="tool-title">
            Herramientas
      </h2>
      <div class="tool-body">
        <div v-for="(tool, index) in tools" :key="index"
             class="tool-item">
          <div class="tool-item-title">
            {{ tool.section }}
          </div>
          <div class="tool-item-body">
            <figure v-for="mytool in tool.items" :key="mytool.image.replace(' ','')"> 
              <img :src="require(`~/assets/img/tools/${mytool.image}`)" height="48" :alt="mytool.name" /> 
              <figcaption>{{ mytool.name }}</figcaption>
            </figure>
          </div>
        </div>
      </div>
  </div>
</template>

<script>
export default {
    name: 'Tools',
    props: {
        tools: {
            type: Array,
            default: () => []
        },
    },

}
</script>

<style lang="scss" scoped>

@import '/assets/css/utilities/_variables';

.tool{

  .tool-title{
    margin-bottom: 1rem;
    display: inline-block;
    border-bottom: 4px solid rgb(255, 205, 164);
  }

  .tool-body{

    .tool-item{
      padding: 1rem;
      margin-bottom: 1rem;
      background-color: #fffcf8;
      border: 1px solid #ffefe8;
      border-radius: 10px;

      .tool-item-title{
        font-size: 1.2rem;
        color: $color-text-strong;
        margin-bottom: .5rem;
        font-weight: 500;
        color: rgb(233, 156, 93);
      }

      .tool-item-body{
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

</style>