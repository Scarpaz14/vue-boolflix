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
            <div><i class="fa-solid fa-star"></i><small>{{number(serie.vote_average)}}</small></div>
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

.card{
    color: white;
    background-color: black;
    padding: 0;
    cursor: pointer;
}
.hover-container{
    display: none;
     height: 100%;
    width: 100%;
    transition: 5s;
    position: absolute;
    overflow: hidden;
}
 .card:hover .hover-container{
    display: block !important;
    background-color: black; opacity: 0.8;
 }

 .card:hover{
    transition: 1s;
    transform: scale(1.05);
    z-index: 100;
 }

 .flags{
    margin-left: 5px;
    font-size: 30px;
    vertical-align: middle;
    border-radius: 50%;
 }




</style>