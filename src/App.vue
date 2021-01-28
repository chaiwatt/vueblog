<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <br>
    <div class="newCat">
      <h3>Add a Cat</h3>
      <div><span>Title: </span><input type="text" v-model="newCat.title"></div>
      <div><span>Message: </span><input type="text" v-model="newCat.msg"></div>
      <div><span>Link: </span><input type="text" v-model="newCat.link"></div>
      <div><span>Image URL: </span><input type="text" v-model="newCat.image"></div>
      
      <cat-card
        :cat="newCat"
      />
    </div>

    
    <cat-card 
      v-for="(item, index) in ListOfCats" 
      v-bind:key="index" 
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
      newCat:{
          title: "Hello Cats",
          msg: "Hello Cats",
          link: "www.cat.com",
          visible: true,
          image: "https://i.imgur.com/Ss75Vfa.jpg"
      },
      ListOfCats: [
        {
          title: "Cats",
          msg: "Hello Cats",
          link: "www.cat.com",
          visible: true,
          image: "https://i.pinimg.com/736x/07/6b/9c/076b9ca43b2521b7990fa0a85b309e73.jpg"
        },
        {
          title: "Big Cats",
          msg: "Hello Big Cats",
          link: "www.bigcat.com",
          visible: true,
          image: "https://i.imgur.com/Ss75Vfa.jpg"
        },
        {
          title: "Bigger Cats",
          msg: "Hello Bigger Cats",
          link: "www.biggercat.com",
          visible: true,
          image: "https://thumbs.dreamstime.com/z/cute-cat-portrait-square-photo-beautiful-white-closeup-105311158.jpg"
        },
        {
          title: "The Bigest Cats",
          msg: "Hello Biggest Cats",
          link: "www.biggestcat.com",
          visible: true,
          image: "https://ic.pics.livejournal.com/ibigdan/8161099/7140450/7140450_original.jpg"
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
.newCat{
  width: 300px;
  padding: 10px;
  margin: 0 auto;
}
</style>
