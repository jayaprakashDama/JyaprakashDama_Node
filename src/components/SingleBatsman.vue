<template>
<td class="TeamPicText" style="background-color:#DBE8D8"><img class="imageTexPad" v-bind:src= "score.teamImage" style="height:20px;width:20px">{{score.playerName}} <label v-if="score.IsRetired" style="text-align:right; color: red;">(R)</label></td>
<td style="background-color:#C3E0E5" >{{score.runs}}</td>
<td style="background-color:#d7d9f2">{{score.innings}}</td>
<td style="background-color:#C3E0E5">{{score.strikeRate}}</td>
<td style="background-color:#d7d9f2">{{score.centuries}}</td>
<td style="background-color:#C3E0E5">{{score.boundaries}}</td>
</template>

<script>
export default{
    name:'SingleBatsman',
    props:{
        score: Array
    }
}

</script>

<style scoped>
.TeamPicText{
    text-align: left;
    padding-left: 10px;
}
.imageTexPad{
    padding-right: 20px;
}
td{
    padding: 10px;
    border: 1px solid rgb(190, 190, 190);
}
</style>