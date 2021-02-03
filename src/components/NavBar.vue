<template>
  <b-navbar 
      toggleable="lg"
      type="dark"
      class="nav"
      variant="faded"
      sticky
      >
        <b-navbar-brand to="/">Daniel Grace</b-navbar-brand>
        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
        <b-collapse id="nav-collapse" is-nav>
          <b-navbar-nav class="ml-auto">
            <b-nav-item href="#About">About Me</b-nav-item>
            <b-nav-item href="#Projects">Projects</b-nav-item>
            <b-nav-item href="#Contact">Contact Me</b-nav-item>
          </b-navbar-nav>
        </b-collapse>
      </b-navbar>
</template>

<script>
export default {

}
</script>

<style>

</style>