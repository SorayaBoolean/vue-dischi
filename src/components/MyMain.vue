<template>
 <div>
  <SingleDisc v-for="(disc, index) in MyMain" :key="index" :disc="disc"/>
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
  

</style>