<template>
    <form @submit.prevent="searchFilm">
        <input class="search mx-3 py-1" type="search" placeholder="Search" aria-label="Search" v-model="dataSelect.filmsSelected">
        <button class="btn btn-outline-danger my-2 my-sm-0" type="submit"><i class="fa-solid fa-magnifying-glass"></i></button>
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
            response.data.results.filter(obj => {
                if(obj.original_language == "en"){
                    obj.original_language = "gb"
                } else if(obj.original_language == "ja"){
                     obj.original_language = "jp"
                }
                this.dataSelect.films = response.data.results;
                console.log(response.data.results)
            });
        }).catch((error) => {
            console.log(error);
        }),

            axios.get('https://api.themoviedb.org/3/search/tv', {
            params: {
                api_key: 'e99307154c6dfb0b4750f6603256716d',
                query: this.dataSelect.filmsSelected,
                language: 'it-IT'
            }
        }).then((response) => {
            response.data.results.filter(obj => {
                if(obj.original_language == "en"){
                      obj.original_language = "gb"
                } else if(obj.original_language == "ja"){
                     obj.original_language = "jp"
                }
                this.dataSelect.series = response.data.results;
                console.log(response.data.results)
            });
        }).catch((error) => {
            console.log(error);
        })
        },
    },  
}

</script>

<style lang="scss" scoped>

input{
    border: 2px solid red;
    border-radius: 10px;
    background-color: lightgray;
    max-width: 50%;
}

.fa-magnifying-glass{
    color:white
}



</style>