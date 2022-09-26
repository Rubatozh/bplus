<template>
  <div class="search-bar">
    {{propdata}}
    <br>
    <!-- v-model passes the input into data -->
    <input type="text" v-model="searchData">
    <button @click="changeText()">Change text</button>
    <br>
    <div class="result"><h3>Your search word is</h3>{{searchData}}</div>
  </div>
</template>

<script>
export default {
  name: 'SearchBar',
  props: {
    propdata: String
  },
  data : function(){
    return{
      searchData: "Please Input a Search word"
    }
  },
  methods:{
    changeText : function(){
      this.searchData = this.searchData+" changed!"
      console.log(this.searchData)
    }
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
div.result h3{
  font-size: larger;
  color:#42b983
}
input{height : 50px;
      width : 200px;      
      border-radius : 5px;
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
