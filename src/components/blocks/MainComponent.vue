<template>
 <main>
     <SectionFilm/>
     <SectionSeries/>
 </main>
</template>

<script>
import SectionFilm from "../sections/SectionFilm.vue";
import SectionSeries from "../sections/SectionSeries.vue";


export default {
    name:'MainComponent',
    components: { 
        SectionFilm,
        SectionSeries, 
    }
}
</script>

<style lang="scss" scoped>

main{
    background-color: #1e2d3b;
    min-height: 100vh
    
}

</style>