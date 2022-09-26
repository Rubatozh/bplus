<template>
  <div class="single-result">
    <span class="title">{{title}}</span>
    <span class="desc">{{desc}}</span><br>

  </div>
</template>

<script>
export default {
  name: 'SingleResult',
  props: {
    title: String,
    desc: String
  },
  data : function(){
    return{

    }
  },
  methods:[

  ]

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .title {font-size: 17px; color:blue}
  .desc {font-size:15px;color:red}
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
