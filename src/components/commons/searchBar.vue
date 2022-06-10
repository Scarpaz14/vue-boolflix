<template>
    <form @submit.prevent="searchFilm">
        <input class="search mx-3 py-1" type="search" placeholder="Search" aria-label="Search" v-model="dataSelect.filmsSelected">
        <button class="btn btn-outline-success my-2 my-sm-0" type="submit">Search Film</button>
    </form>
</template>

<script>
import axios from 'axios';
import dataSelect from '../shared/dataSelect'
export default {
    name: 'FilmCard',
    data(){
        return{
            dataSelect,
            
        }
    },

     methods:{
         searchFilm(){
            axios.get('https://api.themoviedb.org/3/search/movie', {
            params: {
            api_key: 'e99307154c6dfb0b4750f6603256716d',
            query: this.dataSelect.filmsSelected,
            language: 'it-IT'
            }
        }).then((response) => {
        this.dataSelect.films = response.data.results;
        console.log(response.data.results)
        }).catch((error) => {
        console.log(error);
        })
        },
    }
}
</script>

<style lang="scss" scoped>


</style>