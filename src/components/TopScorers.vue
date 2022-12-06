<template>
    <div id="batsmanTable" class="StandingsBox">
        <table>
            <thead>
    <tr>
        <th class="LargeTh">
            Player
        </th>
        <th class="smallTh">
            Runs
        </th>
        <th class="smallTh">
            Innings
        </th>
        <th class="smallTh">
            Strike Rate
        </th>
        <th class="smallTh">
            50's/100's
        </th>
        <th class="smallTh">
            4's/6's
        </th>
    </tr>
</thead >
        <tr v-for="score in scores" :key="score.runs">
            <SingleBatsman :score="score"/>          
        </tr>
        </table>
    </div>
</template>

<script>
import SingleBatsman from "./SingleBatsman.vue"
export default{
    name:'TopScorers',
    components:{
        SingleBatsman
    },
    props:{
        scores: Array
    }
}
</script>

<style scoped>
.contact-details {
            background-color: #8FA6CB;
            padding-top: 5px;
            text-align: left;
            padding-left: 20%;
            padding-bottom: 5px;
        }

.StandingsBox{
    background-color: aqua;
}
thead{
    background-color: black;
    color: aliceblue;
}
th{
    text-align: center;
    border: 1px solid rgb(190, 190, 190);
}
.smallTh{
    width: 400px;
    height: 60px;
}
.LargeTh{
    width: 800px;
    height: 60px;
}
table{
    border-collapse: collapse;
}
</style>