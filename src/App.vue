<template>
  <v-app>
    <v-img
    :cover="true"
    aspect-ratio=3
    gradient="to top left, rgba(190,220,241,.53), rgba(230,32,72,.6)"
    src="@/components/assets/background.jpg"
    >
      <router-view/>
    </v-img>
    <v-footer
        padless
        width="100%"
        app
      >
        <v-card
          flat
          tile
          width="100%"
          class="cyan darken-3 text-center mx-auto"
        >
          <v-card-text>
            <v-row justify="center">
              <v-btn
              v-for="item in items"
              :key="item"
              :href="item.to"
              outlined
              target="_blank"
              icon
              class="mx-4 light-green--text text--accent-3"
              >
                <v-icon size="25px">
                  {{ item.icon }}
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
    items: [
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
</style>
