<template>
  <div >
    <div class="container">
      <div class="discs_container">
          <div class="singleDisc">
            <div class="img_card">
              img
            </div>
            <div class="title_card">
              title
            </div>
            <div class="author_card">
              author
            </div>
          </div>    
      </div>
      
    </div>
  </div>
</template>

<script>

import axios from 'axios'

export default {
    name: 'MyMain',
    data () {
      return {
        MyMain: [],
        endPoint: 'https://flynn.boolean.careers/exercises/api/array/music'
      }
    },

    created () {
      this.getDiscs ();
},
    methods:
      {
        getDiscs () {
          axios.get(this.endPoint)
      .then (response => {
        this.MyMain = response.data
        });
        }
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