<template>
  <div class="experience">
    <h2 class="experience-title">Experiencia</h2>
    <ul class="experience-items">
      <li v-for="(experience, index) in experiences" :key="index"
          class="experience-item">
        <div class="experience-item-box">
          <span class="experience-item-box-period">
            {{ experience.period }}
          </span>
          <span class="experience-item-box-position">
            {{ experience.position }} 
          </span>
          <span class="experience-item-box-company">
            <a :href="experience.company_url" target="_blank">
              {{ experience.company }}
            </a>
          </span>
          <span class="experience-item-box-location">
            <font-awesome-icon icon="map-marker" />
            {{ experience.location }}
          </span> 
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
    name: 'Experience',
    props: {
        experiences: {
            type: Array,
            default: () => []
        },
    }
}
</script>

<style lang="scss" scoped>

@import '/assets/css/utilities/_variables';

li{
  list-style: none;
}

.experience{

    .experience-title{
        margin-bottom: 1rem;    
        display: inline-block;
        border-bottom: 4px solid $color-link-bg;
    }
  
    .experience-items{

        .experience-item{
            margin-bottom: .75rem;
            display: flex;
            flex-direction: row;

            &::before{
              content: "💼";
              padding-top: 1.85rem;
            }

            .experience-item-box{
                display: flex;
                flex-direction: column;
                margin-left: 1rem;

                span{
                    padding: .25rem;
                }

                .experience-item-box-company{
                    padding-top: 0;
                    

                    a{
                        display: inline-block;
                        padding: .25rem .5rem;
                        border-radius: 5px;
                        background-color: rgb(236, 246, 252);
                        color: $color-link-text;

                        &:hover{
                          background-color: $color-link-bg ;
                        }

                    }
                }

                .experience-item-box-position{
                    font-size: 1.1rem;
                    font-weight: bold;
                }

                .experience-item-box-period{
                    font-size: .9rem;
                    font-style: italic;
                    color: $color-text-light;
                }

                .experience-item-box-location{
                    font-size: .9rem;
                    color: $color-text-light;
                }
            }

        }
    }
}

</style>