<template>

<div class="container"> 
   <nav>
    <img src="@/img/Spotify_logo_without_text.svg.webp" alt="logo">
   </nav>
</div>
  
</template>

<script>
export default {
    name:'MyHeader'

}
</script>

<style scoped lang="scss">

nav {
    width: 100%;
    height: 50px;
    background-color: #2E3A46;

        img{
            margin: 5px 5px;
            height: 40px;
            width: 40px;
        }
}

</style>