<template>
    <div class="background">
    </div>

</template>

<script>



export default {
    name:'backroundImage',
   
}
</script>

<style lang="scss" scoped>

.background{
    width: 100%;
    height: calc(100vh);
    position: absolute;
    left: 0;
    background-image: url(../../assets/image/sfondo.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    z-index: -1;
}
</style>