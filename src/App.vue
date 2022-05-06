<template>
  <div class="container">
    <!-- #3 must use the component-->
    <Header mytitle="PlayStation" 
      aboutpage ="Top Games" />
    
    <Playstationbox :games = "games"/>
    <About aboutme="About" />
    



  </div>
</template>
<script>



//import HelloWorld from './components/HelloWorld.vue'
// 1
import Header from './components/Header.vue'
import About from './components/About.vue'
// ----import Bookbox from './components/Bookbox.vue'
import Playstationbox from './components/Playstationbox.vue'


// data url: http://localhost:5555/books , this might be different for you
export default {
  name: 'App',
  components: {
    // 2 register the component 
    Header,
    Playstationbox,
    About
  },

  data(){
    return {
      games: []
    }
  },
  methods: {
    // promises

      async fetchGames(){
         const res= await fetch('https://thawing-lake-69237.herokuapp.com/db.json')
         const data= await res.json()
          console.log(data)
         return data
      }

  },

  async created(){
    this.games = await this.fetchGames()
  }
}
</script>










<style>




@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Montserrat', sans-serif;
  background-color: #e5e5e5;
}
.container {
  max-width: 400px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 0.3em solid black;
  padding: 30px;
  border-radius: 5px;
  background-color: #fca311;
}

div{
  margin-bottom: 0.5em;
}



</style>


