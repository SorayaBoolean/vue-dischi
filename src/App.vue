<template>
  <div id="app">
    <MyHeader @changedGenre="startSearch" :genresList ="genresArray"/>
    <MyMain @genresReady="getGenresList" :genreToSearch="genreToSearch"/> 
  </div>
    
</template>

<script>
import MyHeader from '@/components/MyHeader.vue'
import MyMain from '@/components/MyMain.vue'

export default {
  name: 'App',
  components: {
    MyHeader,
    MyMain
  },
  data () {
    return {
      genresArray: [],
      genreToSearch: ''
    }
  },
  methods: {

    getGenresList (allGenres) {
      this.genresArray = allGenres
    },
    startSearch (genreToSearch) {
      this.genreToSearch = genreToSearch;
    }
  }
}
</script>

<style lang="scss">
   @import '@/styles/general.scss'

</style>
