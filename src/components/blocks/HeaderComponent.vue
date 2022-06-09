<template>
<header>
    <div class="container-fluid d-flex align-items-center">
        <img class="img-fluid" src="https://download.logo.wine/logo/Netflix/Netflix-Logo.wine.png" alt="">
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
    background-color:#303030;
    height: 80px;
    display: flex;
    align-items: center;
}

.container-fluid{
    justify-content: space-between;
}

img{
    width: 100px;
}

</style>