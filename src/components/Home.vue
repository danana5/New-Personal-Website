<template>
    <v-container fill-height>
          <v-sheet
            class="mx-auto"
            tile
            color="#a38c00"
            max-width="600px"
            >
                <v-row
                align="center"
                justify="center"
                class="pa-2"
                >
                    <v-col class="text-center white--text" cols="12">
                        <v-avatar
                        size="200"
                        >
                        <v-img src="../assets/compressed.jpg"></v-img>
                        </v-avatar>
                        <h1 class="display-1 font-weight-thin">Daniel Grace</h1>
                        <h4 class="subheading purple--text text--lighten-2">Computer Science Student</h4>
                        <v-btn
                        class="mx-2"
                        outlined
                        rounded
                        color="white"
                        >
                        About Me
                        </v-btn>
                        <v-btn
                        class="mx-2"
                        outlined
                        rounded
                        color="white"
                        >
                        Projects
                        </v-btn>
                        <v-btn
                        class="mx-2"
                        outlined
                        rounded
                        color="white"
                        >
                        Contact Me
                        </v-btn>
                        <v-btn
                        class="mx-2"
                        outlined
                        rounded
                        href="https://danana5.github.io/"
                        color="white"
                        >
                        Old Website
                        </v-btn>
                    </v-col>
                </v-row>
        </v-sheet>
    </v-container>
</template>

<script>
export default {

}
</script>