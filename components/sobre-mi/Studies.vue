<template>
  <div class="study">
    <h2 class="study-title">Formación Académica</h2>
    <ul class="study-items">
      <li v-for="(study, index) in studies" :key="index"
          class="study-item">
        <div class="study-item-box">
          <span class="study-item-box-year">
            {{ study.year }}
          </span>
          <span class="study-item-box-title">
            {{ study.title }} 
          </span>
          <span class="study-item-box-institution">
            <a :href="study.institution_url" target="_blank">
              {{ study.institution }}
            </a>
          </span>
        </div>
      </li>
    </ul>
  </div>  
</template>

<script>
export default {
    name: 'Studies',
    props: {
        studies: {
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

.study{

    .study-title{
        margin-bottom: 1rem;
        display: inline-block;
        border-bottom: 4px solid rgb(196, 243, 196);
    }
  
    .study-items{

        .study-item{
            margin-bottom: .75rem;
            display: flex;
            flex-direction: row;

            &::before{
              content: "👨‍🎓";
              padding-top: 1.85rem;
            }

            .study-item-box{
                display: flex;
                flex-direction: column;
                margin-left: 1rem;



                span{
                    padding: .25rem;
                }

                .study-item-box-institution{
                    padding-left: .25rem;
                    
                    a{
                       display: inline-block;
                        padding: .25rem .5rem;
                        border-radius: 5px;
                        background-color: rgb(240, 252, 240);
                        color: rgb(59, 180, 59);
                        
                        &:hover{
                          background-color: rgb(196, 243, 196);
                        }
                    }
                }

                .study-item-box-title{
                    font-size: 1.1rem;
                    font-weight: bold;
                }

                .study-item-box-year{
                    font-size: .9rem;
                    font-style: italic;
                    color: $color-text-light;
                }
            }

        }
    }
}

</style>