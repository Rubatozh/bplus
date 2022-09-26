<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <SearchBar propdata="propdata"/>
  <!-- TODO: ResuitSet to render the results -->
  <ResultSet v-bind:resultsList="searchResults"/>
</template>

<script>
import SearchBar from './components/SearchBar.vue'
import ResultSet from "./components/ResultSet.vue"

export default {
  name: 'App',
  components: {
    SearchBar,
    ResultSet
},
  data:function(){
    return{
      searchResults: [
        {title: "helloworld", desc: "First item on the list of results"},
        {title: "helloworld", desc: "Second item on the list of results"},
        {title: "helloworld", desc: "Third item on the list of results"},
        {title: "helloworld", desc: "Fourth item on the list of results"},
      ]
    } 
  },
  methods: {
    doSearch : function(){
      console.log("search to be implemented")
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
