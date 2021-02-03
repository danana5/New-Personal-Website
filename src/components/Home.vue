<template>
    <div>
            <v-parallax
                dark
                src="../assets/background.jpg"
                height= "750"
            >
                <NavBar/>
                <v-row
                align="center"
                justify="center"
                >
                <v-col class="text-center" cols="12">
                    <h1 class="display-1 font-weight-thin mb-4">Daniel Grace</h1>
                    <h4 class="subheading">Computer Science Student</h4>
                </v-col>
                </v-row>
            </v-parallax>
        <v-flex id="About">
            <About/>
        </v-flex>
        <v-flex>
            <Projects/>
        </v-flex>
    </div>

</template>

<script>
import NavBar from "./NavBar"
import About from "./About"
import Projects from "./Projects"
export default {
    components:{
        About,
        NavBar,
        Projects
    }
}
</script>