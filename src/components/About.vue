<template>
  <v-container fill-height>
    <v-sheet
    class="mx-auto"
    tile
    color="#10c020"
    max-width="600px"
    >
    <h1 class="display-1 font-weight-bolder text-center indigo--text">About Me...</h1>
      <v-container fluid fill-height> 
        <v-sheet
        tile
        class="text-center"
        color="orange darken-4"
        max-width="600px"
        >
          <v-avatar
          size="200"
          class="profile mt-2"
          rounded
          >
            <v-img src="../assets/craAndI.jpg"></v-img>
          </v-avatar>
          <h5 class="body-2 white--text pa-1">I am a 21 year old lad from Swords, who has a strong interest in Computer Science, 
            Music, Football and Film.<br><br>I am studying Computer Science in Trinity College Dublin, I've learned so much and I have gained many unique experiences but I've also been fortunate enough to meet many great people and characters whom I am lucky to call friends.
            <br><br>Anyways, I played semi-proffesional football for Drogheda United in the League of Ireland. I am obsessed with music and 
            several artists such as; Flume, deadmau5, Porter Robinson and Brockhampton. Film-wise, I love Christopher Nolan and nearly all of his films, I like Tarantino also and I'm a huge fan of Denis Villeneuve.</h5>
        </v-sheet>
      </v-container>
    </v-sheet>
  </v-container>
</template>

<script>
export default {

}
</script>

<style>

</style>