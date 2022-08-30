<template>
  <div id="app">
    <MyHeader :genresList="genresList"/>
    <MyMain @genresReady ="getGenresList"/> 
  </div>
    
</template>

<script>
import MyHeader from '@/components/MyHeader.vue'
import MyMain from '@/components/MyMain.vue'

export default {
  name: 'App',
  components: {
    MyHeader,
    MyMain, 

  data () {
    return {
      genresList: [ ]
    }
  },
  
  methods: {
    getGenresList (allGenres) {
      this.genresList = allGenres;
    }
  }
  },
  
}
</script>

<style lang="scss">
   @import '@/styles/general.scss'

</style>
