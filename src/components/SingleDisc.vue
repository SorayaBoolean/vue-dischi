<template>
   <div class="container">
      <div class="discs_container">
          <div class="singleDisc">
            <div class="img_card">
              <img :src="disc.poster" alt="poster">
            </div>
            <div class="title_card">
              <h4>{{disc.title}}</h4>
            </div>
            <div class="author_card">
              <p>{{disc.author}}</p>
              <p>{{disc.year}}</p>
            </div>
          </div>    
      </div>
      
    </div>
</template>

<script>
export default {
name: 'SingleDisc',
props: {
    disc: Array 
}
}
</script>

<style scoped lang="scss">
    .container {
      display: flex;
      justify-content: center;
      align-items: center;
      height:700px;
      background-color: #1E2D3B;
  }

  .discs_container{
      display:flex;
      flex-wrap:wrap;
      justify-content: center;
      width:1000px;
      height:600px;
  }

  .singleDisc {
    height: calc(100% / 2);
    width: calc(100% /6);
    margin: 10px;
    border:1px solid white;
    background-color:#2E3A46;

      .img_card {
        margin: auto;
        margin-top:15px;
        height: 130px;
        width: 130px;
        border: 1px solid green;

      }
      .title_card{
        margin-top:15px;
        padding: 15px;
        text-align: center;
        color: white;
        border: 1px solid lightblue;
      }
      .author_card {
        margin-top:15px;
        padding: 15px;
        text-align: center;
        color: grey;
        border: 1px solid orange;
      }
    

  }

</style>