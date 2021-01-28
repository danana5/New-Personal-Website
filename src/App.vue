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
          <router-view/> 
         </transition>       
      </v-content>
      <v-footer
        padless
        width="100%"
        app
        fixed
      >
        <v-card
          flat
          tile
          width="100%"
          class="light-green accent-3 text-center mx-auto"
        >
          <v-card-text>
            <v-row justify="center">
              <v-btn
              v-for="icon in icons"
              :key="icon"
              :href="icon.to"
              outlined
              target="_blank"
              icon
              class="mx-4 white--text"
              >
                <v-icon size="25px">
                  {{ icon.icon }}
                </v-icon>
              </v-btn>
            </v-row>         
          </v-card-text>
        </v-card>
      </v-footer>
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
    ],
  }),
};
</script>
<style>
.nav{
  background-color: #76FF03;
}
#app .nav-item a{
  color:white;
}
</style>