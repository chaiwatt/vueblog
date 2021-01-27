<template>
  <div>
    <hr>
    <div v-if="cat.visible == true" >
      <h2>{{cat.id}}</h2>
        <h1>{{cat.title}}</h1>
        <p>{{cat.msg}}</p>
        <p>{{cat.link}}</p>
    </div>
    <div v-else>
       <strong>{{cat.id}} This '{{cat.title}}' is not available.</strong> 
    </div>
  </div>

</template>

<script>
export default {
  name: 'catCard',
  props: {
    cat: Object
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
