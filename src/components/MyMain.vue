<template>
 <div>
  <div class="container">
    <div class="discs_container">
      <SingleDisc v-for="(disc, index) in MyMain" :key="index" :disc="disc"/>
    </div>
  </div>
  
 </div>
</template>

<script>

import axios from 'axios'
import SingleDisc from '@/components/SingleDisc.vue'

export default {
    name: 'MyMain',
    components: {
    SingleDisc
},
    data () {
      return {
        MyMain: [],
        genres: []
      }
    },

    created () {
      this.getDiscs ();
},
    methods:
      {
        getDiscs () {
          axios.get('https://flynn.boolean.careers/exercises/api/array/music')
      .then (response => {
        this.MyMain = response.data.response;

        this.MyMain.forEach(disc => {
          if(!this.genres.includes(disc.genre)) {
            this.genres.push(disc.genre)
          }
        });
         
        this.$emit ('genresReady', this.genres)

        });

        }
      }
    }

    
</script>


<style scoped lang="scss">

  .container {
      height: 100%;
      background-color: #1E2D3B;
  }

  .discs_container {
    margin: auto;
    padding-top: 30px;
    width: 1000px;
    height: 600px;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
  }

</style>