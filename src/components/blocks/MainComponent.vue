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
    height: calc(100vh);
    padding-top: 100px;
    color: white;
    z-index: 10;
    overflow: hidden;
    overflow-y: auto;
    margin: auto;
}

</style>