<template>
  <!-- <v-app :class="{ 'bg': $route.path === '/login' }"> -->
  <v-app :class="bgClassadd()">
   <router-view></router-view>
  </v-app>
</template>

<style>
.bg{
  background:url(./assets/Bg2.jpg)!important;
   background-position: center !important;
    background-repeat: no-repeat !important;
    background-size: cover !important;
}
a{
  text-decoration: none!important;
}
</style>
<script>
export default {
  name: "App",
data(){
  return{
   
}

},
methods:{
      bgClassadd () {
      if (this.$route.name === 'login') {
      
        return 'bg' 
      }
      else {

        return this.cc
      }  
    }
},
// mounted(){
//   debugger;
//   bgClassadd ()
// }
};
</script>
