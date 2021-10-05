<template>
  <div id="app">
    <Header @selectGenres = "selectedGenres" :genres="genreList"/>
    <Dischi :selectedGenre= "selectedGenre" @genreList="genreListEvent"/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Dischi from './components/Dischi.vue'

export default {
  name: 'App',
  components: {
    Header,
    Dischi
  },
  data() {
    return {
      selectedGenre: "",
      genreList: []
    }
  },
  methods: {
    selectedGenres(selectedGenre) {
      this.selectedGenre = selectedGenre;
    },
    genreListEvent(list) {
      this.genreList = list;
    }
  }
}
</script>

<style lang="scss">
@import './assets/style/common';
</style>
