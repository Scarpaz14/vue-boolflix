<template>
 <main>
     <SectionFilm/>
 </main>
</template>

<script>
import SectionFilm from "../sections/SectionFilm.vue";


export default {
    name:'MainComponent',
    components: { 
        SectionFilm 
    }
}
</script>

<style lang="scss" scoped>

main{
    background-color: #1e2d3b;
    height: calc(100vh + 200px);
    
}

</style>