<template>
<header>
    <div class="container-fluid d-flex align-items-center">
        <img class="img-fluid" src="../../assets/image/logo.png" alt="">
        <SearchBar/>
    </div>


</header>
  
</template>

<script>
import SearchBar from "../commons/searchBar.vue";
export default {
    name: "HeaderComponent",
    components: { 
        SearchBar, 
    }
}
</script>

<style lang="scss" scoped>

header{
    background-color:black;
    height: 100px;
    display: flex;
    align-items: center;
    position: fixed;
    width: 100%;
    z-index: 100;
}

.container-fluid{
    justify-content: space-between;
}

img{
    width: 100px;
}

</style>