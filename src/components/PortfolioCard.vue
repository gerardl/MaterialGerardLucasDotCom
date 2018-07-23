<template>
  <v-card class="my-3" hover>
    <v-card-media
        class="white--text"
        height="170px"
        :src="post.imgUrl">
        <v-container fill-height fluid>
            <v-layout>
                <v-flex xs12 align-end d-flex>
                    <span class="headline">{{ post.title }}</span>
                </v-flex>
            </v-layout>
        </v-container>
    </v-card-media>
    <v-card-text>
        {{ post.content }}
    </v-card-text>
    <v-card-actions>
        <v-btn icon>
            <v-icon>fab fa-github</v-icon>
        </v-btn>
        <v-spacer></v-spacer>
        <v-btn flat class="blue--text">More</v-btn>
    </v-card-actions>
    </v-card>
</template>

<script>
export default {
  name: 'PortfolioCard',
  props: {
    post: {}
  },
  data() {
    return {
        
    }
  },
  created() {
      
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>