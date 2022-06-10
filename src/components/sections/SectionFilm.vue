<template>
  <section>
    <div class="container">
        <h1>FILM:</h1>
        <div class="row" >
            <FilmCard class="col-12 col-sm-6 col-md-3 col-lg-2" v-for="(film,index ) in dataSelect.films" :key="index" :film="film"/>
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