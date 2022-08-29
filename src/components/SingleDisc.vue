<template>
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
  .singleDisc {
    height: 250px;
    width: 150px;
    margin: 10px;
    background-color:rgba(211, 211, 211, 0.195);

      .img_card {
        margin: auto;
        height: 100px;
        width: 150px;
        img{
          padding: 10px 0px;
          margin: 0px 22px;
          height: 100%;
        }
      }
      .title_card{
        text-align: center;
        color: white;
      }
      .author_card {
        text-align: center;
        color: grey;
      }
  }

</style>