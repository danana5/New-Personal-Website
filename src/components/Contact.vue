<template>
  <div>
    <v-container>
      <div class="text-center">
        <h1 class="display-2 font-weight-thin blue-grey--text text--darken-1">Contact Me</h1>
      </div>
      <v-divider/>
        <v-layout wrap>
          <v-flex wrap v-for="(contact, i) in contactLinks" :key="i">
              <ContactList :contact="contact" />
          </v-flex>
        </v-layout>
    </v-container>
  </div>
</template>

<script>
import ContactList from "./ContactList"
export default {
  components: {
    ContactList
  },
  data () {
    return {
      contactLinks: [
        {
          name: "Email",
          value: "daniel.grace44@hotmail.com",
          link: "mailto:daniel.grace44@hotmail.com",
          icon: "mdi-email"
        },
        {
          name: "LinkedIn",
          value: "Daniel Grace",
          link: "https://www.linkedin.com/in/daniel-grace-892963194/",
          icon: "mdi-linkedin"
        },
        {
          name: "Snapchat",
          value: "danana_5",
          link: "https://www.snapchat.com/l/en-gb/",
          icon: "mdi-snapchat"
        },
        {
          name: "Github",
          value: "danana5",
          link: "https://github.com/danana5",
          icon: "mdi-github"
        },
        {
          name: "Facebook",
          value: "Daniel Grace",
          link: "https://www.facebook.com/dananananananananananananana/",
          icon: "mdi-facebook"
        },
        {
          name: "Instagram",
          value: "danana5",
          link: "https://www.instagram.com/danana_5/",
          icon: "mdi-instagram"
        }
      ]
    }
  }
}
</script>