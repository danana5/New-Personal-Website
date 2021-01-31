<template>
  <v-app>
      <b-navbar 
      toggleable="lg"
      type="dark"
      class="nav"
      app
      >
        <b-navbar-brand to="/">Daniel Grace</b-navbar-brand>
        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
        <b-collapse id="nav-collapse" is-nav>
          <b-navbar-nav>
            <b-nav-item to="/about">About Me</b-nav-item>
            <b-nav-item to="/projects">Projects</b-nav-item>
            <b-nav-item to="/contact">Contact Me</b-nav-item>
          </b-navbar-nav>
        </b-collapse>
      </b-navbar>
      <v-content> 
         <transition name="fade" mode="in-out">
          <v-img
          aspect-ratio="8"
          style="height:100%"
          src="./assets/background.jpg"
          >
            <router-view/>
          </v-img>
         </transition>       
      </v-content>
  </v-app>
</template>

<script>
export default {
  name: 'App',
  data: () => ({
    icons :[
      {icon: 'mdi-facebook', to: "https://www.facebook.com/dananananananananananananana/"},
      {icon: 'mdi-twitter', to: "https://twitter.com/Danana_5"},
      {icon: 'mdi-linkedin', to: "https://www.linkedin.com/in/daniel-grace-892963194/"},
      {icon: 'mdi-instagram', to: "https://www.instagram.com/danana_5/"},
      {icon: 'mdi-github', to: "https://github.com/danana5"}
    ]
  }),
};
</script>
<style>
.nav{
  background-color: #187789;
}
#app .nav-item a{
  color:#10c020;
}
#app .navbar-brand {
  color:#10c020;
}
</style>