<template>
  <div class="result-set">
    This is the result set , and its length is: {{countResults()}}
    <br>
    <SingleResult v-for="res in resultsList" :key="res" :title="res.title" :desc="res.desc"/>

  </div>
</template>

<script>
import SingleResult from "./SingleResult.vue"
export default {
  name: 'ResultSet',
  props: {
    resultsList: Array
  },
  components: {
    SingleResult
},
  data : function(){
    return{

    }
  },
  methods:{
    countResults: function(){
      return this.resultsList.length;
    }
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
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
