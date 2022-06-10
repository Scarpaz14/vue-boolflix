<template>
  <div class="card-song my-5 mx-3 py-4">
      <img class="img-fluid" :src="PrefixImg(serie.poster_path)" :alt="serie.author">
      <h3>{{serie.name}}</h3>
      <p>{{serie.original_name}}</p>
      <flag class="flags" :iso="serie.original_language"/>
      <small>{{number(serie.vote_average)}}</small>
  </div>
</template>

<script>
export default {
    name: 'SeriesCard',
    props:{
        serie: Object,
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