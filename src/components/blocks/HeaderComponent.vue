<template>
<header>
    <div class="container-fluid d-flex align-items-center">
        <img class="img-fluid" src="https://download.logo.wine/logo/Netflix/Netflix-Logo.wine.png" alt="">
        <form>
            <input class="search mx-3 py-1" type="search" placeholder="Search" aria-label="Search">
            <button class="btn btn-outline-success my-2 my-sm-0" type="submit">Search</button>
        </form>
    </div>


</header>
  
</template>

<script>
export default {
    name: 'HeaderComponent'
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