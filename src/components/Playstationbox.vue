<template>
    
    <div class="gamebox">
        
        <div v-for="game in games" :key="game.id" >
            <Game :game="game"/>
     
                <!--<div><h3> {{game[0].title}} </h3></div>
                <div><h3> {{game[1].title}} </h3></div>
                <div><h3> {{game[2].title}} </h3></div>
                <div><h3> {{game[3].title}} </h3></div>
                <div><h3> {{game[4].title}} </h3></div>-->
                
        
        </div>
       
    </div>

</template>

<script>

import Game from './Game.vue'
export default{

    name: 'Playstationbox',
    components: {
        Game
    },
    props: {
        games: Array
    }
}

</script>

<style scoped>

.gamebox{

    background-color:#14213d;
    padding: 1em;
    color: yellow;
}

</style>
