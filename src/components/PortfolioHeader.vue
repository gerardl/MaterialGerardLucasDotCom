<template>
    <div class="text-xs-center mb-2">
        <v-avatar size="125px">
            <img class="img-circle elevation-7 mb-1" src=".././assets/gl_pic.jpg">
        </v-avatar>
        <div class="headline"><span class="font-weight-bold">Gerard Lucas</span></div>
        <div class="subheading text-xs-center grey--text pt-1 pb-3">Senior Software Developer and Project Manager</div>
        <v-layout justify-space-between>
            <v-btn flat color="primary" href="https://www.linkedin.com/in/gerard-lucas-981267a0" target="_blank">
                <v-icon color="light-blue" left>fab fa-linkedin</v-icon>LinkedIn
            </v-btn>
            <v-btn flat color="primary" href="https://github.com/gerardl" target="_blank">
                <v-icon color="black" left>fab fa-github</v-icon>Github
            </v-btn>
            <v-btn flat color="primary" href="mailto:glucas@conperio.com" target="_blank">
                <v-icon color="grey darken-2" left>mail</v-icon>Mail
            </v-btn>
        </v-layout>
    </div>
</template>

<script>
export default {
  name: 'PortfolioHeader'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    a {
        text-decoration: none;
    }
</style>