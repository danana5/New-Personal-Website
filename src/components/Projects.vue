<template>
  <div>
    <v-container>
        <div class="text-center">
          <h1 class="display-2 font-weight-thin blue-grey--text text--darken-1">My Projects</h1>
        </div>
        <v-divider/>
        <v-layout wrap>
          <div v-for="(app, i) in apps" :key="i">
            <v-card flat color="transparent" max-width="350px">
              <v-card-title>
                <v-layout>
                  <v-flex>
                    <v-card
                      :href="app.link"
                      target="_blank"
                      elevation="5"
                      style="border-radius: 20px"
                      width="100px"
                      height="100px"
                    >
                      <v-img slass="mx-auto" :src="logo(app.logo)"/>
                    </v-card>
                  </v-flex>
                  <v-flex xs7>
                    <div>{{app.name}}</div>
                    <div>
                      <v-chip small pill color="blue" dark>{{app.price}}</v-chip>
                    </div>
                    <template v-for="(platform, i) in app.platforms">
                      <v-btn :href="platform.link" target="_blank" icon :key="i">
                        <v-icon>{{platform.icon}}</v-icon>
                      </v-btn>
                    </template>
                  </v-flex>
                </v-layout>
              </v-card-title>
              <v-card-text>
                <div>{{app.description}}</div>
                <div class="title mt-2">Technologies Used</div>
                <v-layout>
                  <template v-for="(tech, i) in app.tech">
                    <v-flex xs3 :key="i">
                      <div class="text-center">
                        <v-btn icon>
                          <v-icon>{{tech.icon}}</v-icon>
                        </v-btn>
                        <div class="caption">{{tech.name}}</div>
                      </div>
                    </v-flex>
                  </template>
                </v-layout>
                <div v-if="app.code">
                  <div class="title mt-2">Code</div>
                  <v-btn icon :href="app.code" target="_blank">
                    <v-icon>mdi-github</v-icon>
                  </v-btn>
                </div>
              </v-card-text>
            </v-card>
          </div>
        </v-layout>
    </v-container>
  </div>
</template>

<script>
export default {
  data () {
      return {
        apps: [
          {
          name: "CEQ Website",
          price: "Free-Lance",
          logo: "ceq.gif",
          platforms: [
            {
              icon: "mdi-web",
              link: "https://www.carrickminesequestrian.ie/"
            }
          ],
          description:
            "During the summer of 2020, 2 colleagues and I, built a fully responsive and functioning website with integrated eCommerce. I was the lead designer on the project. Our client wanted to be able to easily edit and update the website on his own volition. For this reason we decided to use SquareSpace to build the website. During the project I worked closely with a proffesional photographer to design and craft content to our client's specific needs.",
          tech: [
            {
              name: "Squarespace",
              icon: "mdi-square-rounded-outline",
              link: ""
            },
          ],
          code: ""
        },
        {
          name: "DIF Dashboard",
          price: "Free-Lance",
          logo: "dif.png",
          platforms: [
            {
              icon: "mdi-web",
              link: "https://dif-dashboard.vercel.app/#/"
            }
          ],
          description:
            "I designed and developed the DIF Dashboard during the January break of 2021 for Dublin Indoor Football in order to help the company realise their goal of becoming paperless by 2022. The app is written in Vue.js using the Vuetify framework. The app uses Firebase's scalable NoSQL cloud database, Cloud Firestore, to store and sync data and uses Firebase Authentication for user authentication. During my time developing the DIF Dashboard I learned how to use Vue.js and gained a further understanding of Node.js.",
          tech: [
            {
              name: "Vue.js",
              icon: "mdi-vuejs",
              link: ""
            },
            {
              name: "Vuetify",
              icon: "mdi-vuetify",
              link: ""
            },
            {
              name: "Firebase",
              icon: "mdi-firebase",
              link: ""
            },
            {
              name: "NPM",
              icon: "mdi-npm",
              link: ""
            }
          ],
          code: "https://github.com/danana5/DIF-Dashboard"
        },
        {
          name: "Discord Bot",
          price: "Personal Use",
          logo: "discord.png",
          platforms: [
            {
              icon: "mdi-discord",
              link: "https://discord.com/api/oauth2/authorize?client_id=762677013110194217&permissions=8&scope=bot"
            }
          ],
          description:
            "At the start of my third year in college, I decided to make a Discord bot in Python which will help me and my friends through our time doing online lectures. The bot in its current iteration has various commands to display our timetable on any given day and then provide links to the online lecture rooms for any given module. During my time developing the bot I learned how to write Python code and work with the Discord.py API documentation. ",
          tech: [
            {
              name: "Python",
              icon: "mdi-language-python",
              link: ""
            },

          ],
          code: "https://github.com/danana5/Personal-Discord-Bot"
        },
        {
          name: "GitHub Visualiser",
          price: "College Assignment",
          logo: "git.png",
          platforms: [
            {
              icon: "mdi-web",
              link: ""
            }
          ],
          description:
            "As a part of my Software Engineering module in my 3rd year of college, we were tasked to write a single page web app which queries the GitHub REST API and then visualises the data which is recieved on relevant graphs etc. The program is written in React.js using Node Packet Manager.",
          tech: [
            {
              name: "React.js",
              icon: "mdi-react",
              link: ""
            },
            {
              name: "NPM",
              icon: "mdi-npm",
              link: ""
            }
          ],
          code: "https://github.com/danana5/DIF-Dashboard"
        },
        {
          name: "IBM: Annotator",
          price: "College Assignment",
          logo: "ibm.png",
          platforms: [
            {
              icon: "mdi-web",
              link: ""
            }
          ],
          description:
            "During my Software Engineering Project module in my 2nd year of college, My group and I were given this project. The project was to develop a software that would enable surgeons to highlight regions of interest during surgery to identify cancerous cells. Our part of the project was to design and build the UI and the annotation section of the project. The entire project was written in JavaScript and uses several open source packages. ",
          tech: [
            {
              name: "React.js",
              icon: "mdi-react",
              link: ""
            },
            {
              name: "NPM",
              icon: "mdi-npm",
              link: ""
            }
          ],
          code: "https://github.com/CSU33013-SWENG-Group-9/Easy-Annotator"
        },
        ]
    }
  },
  methods: {
    logo(name) {
      return require("../assets/" + name);
    }
  }
}
</script>

<style>

</style>