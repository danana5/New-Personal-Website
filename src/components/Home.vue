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
                    <h4 class="subheading mb-4">Computer Science Student</h4>
                </v-col>
                </v-row>
            </v-parallax>          
        <v-flex id="About">
            <About/>
        </v-flex>
        <v-flex id="Projects">
            <Projects/>
        </v-flex>
        <v-flex id="Contact">
            <Contact/>
        </v-flex>
        <Footer/>
    </div>

</template>

<script>
import NavBar from "./NavBar"
import About from "./About"
import Contact from "./Contact"
import Footer from "./Footer"
import Projects from "./Projects"
export default {
    components:{
        About,
        NavBar,
        Projects,
        Footer,
        Contact
    },
}
</script>