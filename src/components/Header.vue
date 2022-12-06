<template>
<div id="home" class="Navigation">
    <nav class="navbar">
     <div>
       <img src="https://i0.wp.com/logotaglines.com/wp-content/uploads/2016/07/Ipl-logo.jpg?fit=1024%2C729&ssl=1"  style="width:140px;height:120px"/>
     </div>
     <ul class="nav-links">
       <div class="menu">
         <li><a href="#home">Home</a></li>
         <li><a href="#batsmanTable">Standings</a></li>
         <li><a href="#contact">Contact</a></li>
       </div>
     </ul>
   </nav>
</div>
</template>

<script>

export default{
    name:'MyHeader',
    props:{ title:{type: String, default: "My app title"},
            author:{type: String, default: "Author Name"}

    },
    methods:{
        onClick(){
            console.log("We just clicked")
        }
    }
}

</script>
<style scoped>
.Navigation{
    size: 1vmax;
}
li {
 list-style: none;
}
.navbar {
 display: flex;
 align-items: center;
 justify-content: space-between;
 padding: 20px;
 background-color: teal;
 color: #fff;
}
.nav-links a {
 color: #fff;
}
.menu {
 display: flex;
 gap: 1em;
 font-size: 18px;
}
.menu li:hover {
 background-color: #4c9e9e;
 border-radius: 5px;
 transition: 0.3s ease;
}
.menu li {
 padding: 5px 14px;
}
</style>
