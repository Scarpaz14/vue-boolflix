<template>
  <div class="card-song my-5 mx-3 py-4">
      <img class="img-fluid" :src="PrefixImg(film.poster_path)" :alt="film.author">
      <h3>{{film.title}}</h3>
      <p>{{film.original_title}}</p>
      <flag class="flags" :iso="film.original_language"/>
      <small>{{number(film.vote_average)}}</small>
  </div>
</template>

<script>
export default {
    name: 'FilmCard',
    props:{
        film: Object,
    },

    

    methods:{
        PrefixImg(prefix){
            let codeimg = "https://image.tmdb.org/t/p/w500"
            return codeimg + prefix;
        },

        number(numberrounded){
            return Math.round(numberrounded)
        },
    },

    

}
</script>

<style lang="scss" scoped>

.card-song{
    color: white;
    background-color: #2e3a46 ;

}
</style>