<template>
  <div>
    <v-container class="text-center">
        <h1 class="display-2 font-weight-thin blue-grey--text text--darken-1"> About Me</h1>
        <v-divider/>
        <v-card flat max-width="900" class="mx-auto" color="transparent">
          <div class="body-1 blue-grey--text text--darken-1">Hello! I am Dan, I am a 21 year old lad from Swords in third year Computer Science at Trinity College Dublin. 
              I've learned so much and I have gained many unique experiences but I've also been fortunate enough to meet many great people and characters whom I am lucky to 
              call friends.<br><br>I am a front-end developer but with a strong interest also with full stack development. I have experience using React.js and Vue.js 
              aswell as Python, Java and C.<br><br>Anyways, I played semi-proffesional football for Drogheda United in the League of Ireland. I am obsessed with music and several 
              artists such as; Flume, deadmau5, 
              Porter Robinson and Brockhampton. Film-wise, I love Christopher Nolan and nearly all of his films, I like Tarantino also and I'm a huge fan of Denis Villeneuve.
          </div>
          <div class="mt-8" width="100">
          <v-carousel
          cycle
          interval=5000
          >
            <v-carousel-item
            v-for="(item,i) in items"
            :key="i"
            :src="logo(item.src)"
            ></v-carousel-item>
          </v-carousel>
        </div>
        </v-card>
    </v-container>
  </div>
</template>

<script>
export default {
  data () {
      return {
          items: [
            {src: "compressed.jpg"},
            {src: "cra.jpg"},
            {src: "pub.jpg"},
            {src: "park.jpg"},
            {src: "elephant.jpg"},
            {src: "bro.jpg"},
            {src: "bernie.jpg"},
          ],
      }
  },
  methods: {
    logo(name) {
      return require("../assets/" + name)
    }
  }
}
</script>