<template>
    <div :class="showMenu? 'menu-wrapper' : '' "  @click="$emit('onShowMenu')">
        <nav class="menu"
             :class="showMenu ? 'menu-block' : 'menu-none' ">
            <div v-for="(item,index) in menu"
                :key='index'
                class="menu-item"
                @click="$emit('onShowMenu')">
                <nuxt-link :to="item.link">{{ item.text }}</nuxt-link>
            </div>
        </nav>
    </div>
</template>

<script>

export default {
    name: 'AppMenu',
    props: {
        displayNone: {
            type: Boolean,
            default: false
        }
    },
    data(){
        return {
            menu: [
                { text: 'Inicio'    , link: '/'          },
                { text: 'Blog'      , link: 'blog'      },
                { text: 'Sobre mi'  , link: 'sobre-mi'  },
                { text: 'Contacto'  , link: 'contacto'  },
            ],
            active: true,
            cerrar: false,
        }
    },
    computed:{
        showMenu(){
            return this.displayNone && this.active;
        },   
    },
    beforeMount() {
        window.addEventListener('resize', this.onResize)
    },
    methods:{
        onResize(e) {
            const dynamicWidth = e.srcElement.innerWidth
            if(dynamicWidth> 768)
                this.active = false;
            else
                this.active = true;
        },
        onClose(){
            this.cerrar = true;
        }
    },

}
</script>

<style lang="scss" scoped>

@import '/assets/css/utilities/_variables';

.menu-wrapper{
    position: absolute;
    width: 100%;
    height: 100vh;
    top:0;
    bottom: 0;
    left: 0;
    right: 0;
    background-color: transparent;
    z-index: 10;
}

.menu-block{
    display: inline-block;
}

.menu-none{
    display: none;
}

.menu{
    position: absolute;
    flex-direction: column;
    background: white;
    border-radius: 10px;
    top: 90px;
    right: 70px;
    box-shadow: rgba(17, 17, 26, 0.2) 0px 4px 50px, rgba(17, 17, 26, 0.05) 0px 20px 50px;
    padding: 0.8rem;
    font-size: 1.25rem;

    @media (min-width: $breakpoint-smallscreen) {
        position: sticky;
        display: flex;
        flex-direction: row;
        background: transparent;
        border-radius: 0;
        top: 80px;
        right: 60px;
        box-shadow: none;
        padding: 0rem;
    }

    .menu-item{
        margin: 0rem;

        a{
            box-sizing: border-box;
            font-weight: 500;
            display: block;
            padding: .5rem 1rem;
            text-decoration: none;
            border-width: 0;
            border-radius: 10px;

            &:hover{
                border-width: 0;
                background-color: #f8efd2;
            }
        }

        .nuxt-link-exact-active {
            border-width: 0;
        }


        @media (min-width: $breakpoint-smallscreen) {
            margin-left: 1.5rem;
            padding: 0;
            font-size: 1rem;
            
            a{
                box-sizing: border-box;
                font-weight: 500;
                display: block;
                padding: .5rem 0rem;
                text-decoration: none;
                border-bottom: 4px solid transparent;
                border-radius: 0;

                &:hover{
                    border-bottom: 4px solid #ffec3f;
                    background-color: transparent;
                }
            }

            .nuxt-link-exact-active {
                border-bottom: 4px solid #ffec3f;
            }
        }
    }
}

</style>