<template>
    <div class="footer-content container">
        <nav class="footer-content-menu">
            <div v-for="(item,index) in menu"
                :key='index'
                class="menu-item">
                {{ item.icon }} <nuxt-link :to="item.link">{{ item.text }}</nuxt-link>
            </div>
        </nav>

        Copyright © {{ year }} - Cristhian Mesta <br>
        <div class="footer-content-redes">
            <a class="text-github"
               href="https://github.com/cristhianmesta"
               target="_blank">
                <font-awesome-icon :icon="['fab', 'github']" />
            </a>
            <a class="text-linkedin"
               href="https://www.linkedin.com/in/cristhianmesta"
               target="_blank">
                <font-awesome-icon :icon="['fab', 'linkedin']"  />
            </a>
            <a class="text-twitter"
               href=""
               target="_blank">
                <font-awesome-icon :icon="['fab', 'twitter']"  />
            </a>
        </div>
    </div>
</template>

<script>
export default {
    name: 'AppFooter',
    data(){
        return {
            year: new Date().getFullYear(),
            menu: [
                { text: 'Inicio'    , link: '/'        , icon: '🏠' },
                { text: 'Blog'      , link: 'blog'     , icon: '📝'  },
                { text: 'Sobre mi'  , link: 'sobre-mi' , icon: '🤓'  },
                { text: 'Contacto'  , link: 'contacto' , icon: '📫' },
            ],
        }
    }
}
</script>

<style lang="scss" scoped>

@import '/assets/css/utilities/_variables';

.footer-content{
    color: $color-text-light;
    font-size: .925rem;
    text-align: center;


    @media (min-width: $breakpoint-widescreen) {
        padding-bottom: 2rem;
    }

    .footer-content-menu{
        display: flex;
        gap: 1.5rem;
        justify-content: center;
        padding-bottom: 2rem;

        a{
            font-size: .7rem;
            border-bottom: 2px solid $color-logo-secondary;

            @media (min-width: $breakpoint-tablet) {
                font-size: .9rem;
            }

            &:hover{
                background-color: rgb(255, 247, 212)
            }
        }
    }

    .footer-content-redes{
        margin-top: 1rem;
        
        a{
            font-size: 1.5rem;
            padding-left: .5rem;
            padding-right: .5rem;
        }
    }
}

</style>