<template>
    <div  class="terminal">
        <div class="terminal-bar-title">
            <div>cristhianmesta.com</div>
            <div>
                <span class="text-green">●</span>
                <span class="text-orange">●</span>
                <span class="text-red">●</span>
            </div>
        </div>
        <div class="terminal-work-area">
            <h2>
                <span class="text-purple">cm></span>
                <span class="text-turquoise">blog></span>
                <span class="text-yellow">nuevo_</span>
            </h2>
            <div class="notice">
                <nuxt-link to="/blog/hola-mundo">
                    <div class="notice-image">
                        <img :src="require(`~/assets/img/posts/hola-mundo.jpg`)"  :alt="'Hola mundo'" />
                    </div>
                    <div class="notice-content">
                        <div class="notice-meta">
                            <font-awesome-icon :icon="['fas', 'calendar']"  /> 06-01-2021
                        </div>
                        <div class="notice-title">
                        ¡Hola mundo!
                        </div>
                        <div class="notice-body">
                            Hoy en día, programar debe considerarse una displina indispensable del conocimiento.
                        </div>
                    </div>
                </nuxt-link>
            </div>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>

@import '/assets/css/utilities/_variables';

.terminal{
    background-color: rgb(202, 202, 202);
    border-radius: 10px;
    box-shadow: rgba(0, 0, 0, 0.4) 0px 30px 90px;
    display: flex;
    flex-direction: column;
    overflow: hidden;
    

    .terminal-bar-title{
        background: rgb(85,85,85);
        background: linear-gradient(5deg, rgb(194, 194, 194) 0%, rgb(224, 224, 224) 100%);
        padding: 0.5rem 1rem;
        display: flex;
        justify-content: space-between;
    }

    .terminal-work-area{
        color: white;
        padding: 1rem 1rem 2rem 1rem ;
        background-color: rgb(43, 43, 71);

        h2{
            margin-bottom: 1rem;
            font-family: $font-mono;
            font-style: italic;

        }
    }
}

.notice{
    display: flex;
    flex-direction: column;

    .notice-image{
      img{
        width: 100%;
        border-radius: 5px;
      }
    }

    .notice-content{
        padding: 1px;
  
        .notice-title{
            font-size: 2rem;
            margin: .5rem 0;
            font-weight: bold;
            font-family: $font-title;

            &:hover{
                text-decoration: underline;
            }
        }

        .notice-body{
            font-size: 1.1rem;
        }

        .notice-meta{
            color: rgb(173, 173, 173);
            font-size: 0.8rem;
            margin-top: 1rem;
        }
    }
}

</style>