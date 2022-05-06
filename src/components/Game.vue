<template>
    <div>
       <h2>{{game.title}}</h2>
       <h4>{{game.year}} - {{game.company}}</h4>
       <h4>{{game.genre}} - {{game.rating}} star</h4>
    </div>
   
   
</template>

<script>

export default{
    name: 'Game',
    props:{
        game: Array
    }
   
}
</script>

<style scoped>

h4{
    margin: 2px;
}


div{
    background-color: #ffd60a;
    color: #003566;
    padding: 1em;
}



</style>