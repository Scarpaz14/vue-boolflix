<template>
  <section>
    <div class="container">
        <div class="row">
            <h1>Serie TV:</h1>
            <SeriesCard class="col-12 col-sm-6 col-md-3 col-lg-3" v-for="(serie,index) in dataSelect.series" :key="index" :serie="serie"/>
        </div>
    </div>
  </section>
</template>

<script>
import SeriesCard from '../commons/Seriescard.vue'
import dataSelect from '../shared/dataSelect';
export default {
    name: 'SectionSeries',
    data() {
        return {
            dataSelect,
            SeriesCard
            
        
        };
    },
    components: {
        SeriesCard
    },
    
    } 
</script>

<style lang="scss" scoped>

h1{
    color:white;
}
</style>