<template>
  <a :href="cat.link" v-if="cat.title">
      <div :class="[cat.visible ? 'visible' : 'invisible','catCard']">
        <div v-if="cat.visible == true" >
          <h2>{{cat.id}}</h2>
          <img v-if="cat.image" class="catImage" :src="cat.image" alt="">
            <h1>{{cat.title}}</h1>
            <p>{{cat.msg}}</p>
            <p>{{cat.link}}</p>
        </div>
        <div v-else>
          <h2>{{cat.id}}</h2>
          <img class="catImage" :src="cat.image" alt="">
            <h1>{{cat.title}}</h1>
        </div>
      </div>
  </a>

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
.catCard{
  display: inline-flex;
  border: 1px solid #e6e6e6;
  width: 300px;
  height: 300px;
  justify-content: center;
}
.visible{
  background: green;
}
.invisible{
 background: grey;
}
a {
  text-decoration: none;
  color:whitesmoke
}
.catImage {
  width: 100px;
  height: 100px;
}
</style>
