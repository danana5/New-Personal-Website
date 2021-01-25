<template>
  <v-app>
    <v-img
    :cover="true"
    aspect-ratio=2
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
            <v-icon size="25px" v-for="item in items"
            :key="item"
            :to="item.to"
            outlined
            class="mx-4 light-green--text text--accent-3">
              {{ item.icon }}
            </v-icon>
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
        {icon: 'mdi-facebook', to: "/"},
        {icon: 'mdi-twitter', to: "/"},
        {icon: 'mdi-linkedin', to: "/"},
        {icon: 'mdi-instagram', to: "/"},
      ],
  }),
};
</script>
<style>
</style>
