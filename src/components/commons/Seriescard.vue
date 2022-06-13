<template>
 <div class="card my-5">
        <div class="text-center" v-if="serie.poster_path==null">
        <img class="img-fluid" src="https://download.logo.wine/logo/Netflix/Netflix-Logo.wine.png" alt="">
        <h3>IMMAGINE NON DISPONIBILE</h3>
        </div>
        <img class="img-fluid" :src="PrefixImg(serie.poster_path)" :alt="serie.author" v-else>
        <div class="hover-container">
            <small>Title:</small><h3>{{serie.name}}</h3>
            <small>Original title:</small><h3>{{serie.original_name}}</h3>
            <small>Overwiew:</small><p class="overview">{{serie.overview}}</p>
            <small>Language:</small><flag class="flags" :iso="serie.original_language"/>
            <div class=" vote mt-2">
                <small>Vote:</small>
                <span v-for="star in number(serie.vote_average)" :key="star">
                <i class="fa-solid fa-star"></i>
                </span>
                <span v-for="star in ( 5 - number(serie.vote_average))" :key="star">
                <i class="fa-regular fa-star"></i>
                </span>
            </div>
        </div>
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
            let codeimg = "https://image.tmdb.org/t/p/w342";
            return codeimg + prefix;
        },

        number(numberrounded){
            return Math.ceil(numberrounded/2);
        },
    },

    

}
</script>

<style lang="scss" scoped>
@import '../../assets/style/mixins.scss';

.card {
   @include card
}

.hover-container{ 
   @include hover-container
}
 .card:hover .hover-container{
    @include in-hover
 }

 .card:hover{
    @include card-hover 
 }

 .flags{
    @include flags
 }

 .vote{

    .fa-star{
        color:yellow
    }
 }




</style>