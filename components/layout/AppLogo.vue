<template>
    <div class="logo">
        <a href="/">
            <img src="/logo.svg" title="cristhianmesta.com"/>
        </a>
    </div>
</template>

<script>
export default {
    name: 'AppLogo'
}
</script>

<style lang="scss" scoped>

.logo{
    display: inline-block;

    a{
        display: block;

        img{
            padding-top: 5px;
            width: 80px;
            position: relative;
        }
    }

}

</style>