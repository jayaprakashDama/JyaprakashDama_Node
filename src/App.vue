<template>
 <MyHeader title= "Indian Premier League- Top Scorers" author="Jayapakash" />
 <TopScorers :scores="scores"/>
 <MyFooter/>
</template>

<script>
import MyHeader from './components/Header.vue'
import TopScorers from './components/TopScorers.vue'
import MyFooter from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    MyHeader,
    TopScorers,
    MyFooter
  },


data(){

  return{
    scores:[]
  }

},


methods:{

  async fetchScores(){
    const res = await fetch('https://ijayaprakash.herokuapp.com/api')
    const data = await res.json()
    console.log(data)
    return data
    }
  },

  async created(){
  this.scores = await this.fetchScores()
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
}
body{
  margin: 0px;
  background-color: black;
}
</style>
