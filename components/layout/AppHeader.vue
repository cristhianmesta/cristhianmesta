<template>
   <div class="container-header">
        <div class="logotipo">
            <AppLogo/> 
        </div>
        <AppMenu :display-none = "showMenu" @onShowMenu="close()" />
        <AppMenuButton @onShowMenu="show()" />
    </div>
</template>

<script>


export default {
    name: "AppHeader",
    data(){
        return{
            showMenu: false
        }
    },
    methods:{
        show(){
            this.showMenu =  !this.showMenu;
        },
        close(){
            this.showMenu =  false;
        }
    }
}

</script>

<style lang="scss" scoped>

@import '/assets/css/utilities/_variables';

.container-header{
    width: 100%;
    margin: 0 auto;
    padding: 2rem 1.5rem 1em 1.5rem;
    display: flex;
    flex-flow: row nowrap;
    justify-content: space-between;  

    @media (min-width: $breakpoint-smallscreen) {
        padding: 2rem 2rem 1rem 2rem;
    }

    @media (min-width: $breakpoint-widescreen) {
        width: 950px;
        padding: 3em 0 1rem 0;
    }

    @media (min-width: $breakpoint-extrawidescreen) {
        width: 1150px;
    }
}

.logotipo{
    display: flex;
}

</style>>