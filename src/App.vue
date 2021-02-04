<template>
  <v-app>
    <transition name="fade" mode="out-in">         
      <Home/>
    </transition>       
  </v-app>
</template>

<script>
import Home from "./components/Home"
export default {
  name: 'App',
  components:{
    Home,
  },
  data: () => ({
    
  }),
};
</script>
<style>
#app .nav-item a{
  color:white;
}
#app .navbar-brand {
  color:white;
}
</style>