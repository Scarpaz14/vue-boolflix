<template>
  <div class="card-song my-5 mx-3 py-4">
      <img class="img-fluid" :src="film.poster_path" :alt="film.author">
      <h3>{{film.title}}</h3>
      <p>{{film.release_date}}</p>
      <p>{{film.original_language}}</p>
      <small>{{film.overview}}</small>
  </div>
</template>

<script>
export default {
    name: 'FilmCard',
    props:{
        film: Object,
    }

}
</script>

<style lang="scss" scoped>

.card-song{
    color: white;
    background-color: #2e3a46 ;

}
</style>