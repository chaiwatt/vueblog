<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <cat-card 
      v-for="item in ListOfCats" 
      v-bind:key="item.id" 
      :cat="item"
    />
  </div>
</template>

<script>
import catCard from './components/catCard'

export default {
  name: 'App',
  data: function(){
    return {
      ListOfCats: [
        {
          id: 1,
          title: "Cats",
          msg: "Hello Cats",
          link: "www.cat.com",
          visible: true
        },
        {
          id: 2,
          title: "Big Cats",
          msg: "Hello Big Cats",
          link: "www.bigcat.com",
          visible: true
        },
        {
          id: 3,
          title: "Bigger Cats",
          msg: "Hello Bigger Cats",
          link: "www.biggercat.com",
          visible: false
        },
        {
          id: 4,
          title: "The Bigest Cats",
          msg: "Hello Biggest Cats",
          link: "www.biggestcat.com",
          visible: true
        },
      ]  
    }
  },
  components: {
    catCard
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
