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
    min-height: 100vh
    
}

</style>