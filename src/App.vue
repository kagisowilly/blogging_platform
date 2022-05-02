<template>
<div class="dashboard">
  <div class="sideB">
   <Sidebar />  
  </div>
   <div>
     <Navbar /> 
    <router-view/> 
   </div>
 
</div>

  
</template>

<script>
import Sidebar from "@/components/Sidebar.vue";
import Navbar from "@/components/Navbar.vue";

export default {
  components:{
    Sidebar, Navbar
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
.sideB{
    background-color: rgb(81, 81, 81);
}

.dashboard {
    display: grid;
    grid-template-columns: 200px 5fr;
    background-color: rgb(205, 205, 205);
    height: 100vh;
    width: 100vw;
}

.content {
    background-color: white;
    border-radius: 10px;
    margin: 6px 6px 6px 0px;
}
@media all and (max-width: 600px) {
.dashboard {

    grid-template-columns: 70px 5fr;

}
}
</style>
