<template>

<div class="container"> 
   <nav>
    <img src="@/img/Spotify_logo_without_text.svg.webp" alt="logo">

    <div class="select_container">
        <select name="genere" id="genere">
            <option v-for="(genre, index) in genresList" :key="index" :value="genre">{{genre}}</option>
        </select>
    </div>
    
   </nav>
</div>
  
</template>

<script>
export default {
    name:'MyHeader',
    props: {
        genresList: Array
    }

}
</script>

<style scoped lang="scss">

nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
    height: 50px;
    background-color: #2E3A46;

        img{
            margin: 5px 5px;
            height: 40px;
            width: 40px;
        }

        .select_container{
            margin-right: 10px;

            select{
                width: 150px;
            }
        }
}

</style>