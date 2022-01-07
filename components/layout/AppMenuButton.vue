<template>
    <div class="menu-burger">
        <button @click="$emit('onShowMenu')">
            <font-awesome-icon icon="ellipsis-v" />
        </button> 
    </div>
</template>

<script>

export default {
    name: 'AppMenuButton'
}

</script>

<style lang="scss" scoped>

@import '/assets/css/utilities/_variables';

.menu-burger{
    
    z-index: 999;
    display: block;

    button {
        font-size: 1.2rem;
        background-color: #f8efd2;
        color: #FCD359;
        border-radius: 22.5px;
        width: 45px;
        height: 45px;
        padding: 12.5px;
        text-align: center;
        border: none;
        cursor: pointer;

        &:hover{
            background-color: #FCD359;
            color: #fcf8ed;        
        }
    }

    @media (min-width: $breakpoint-smallscreen) {
        display: none;
    }
}

</style>