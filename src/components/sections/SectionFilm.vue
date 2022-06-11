<template>
  <section>
    <div class="container">
        <div class="row">
            <h1>Film:</h1>
            <FilmCard class="col-12 col-sm-6 col-md-3 col-lg-3" v-for="(film,index ) in dataSelect.films" :key="index" :film="film"/>
        </div>
    </div>
  </section>
</template>

<script>

import FilmCard from '../commons/FilmCard.vue'
import dataSelect from '../shared/dataSelect';
export default {
    name: 'SectionFilm',
    data() {
        return {
            dataSelect,
            FilmCard,
            
        
        };
    },
    components: {
        FilmCard,
    },
    
    } 
</script>

<style lang="scss" scoped>
h1{
    color:white;
}
</style>