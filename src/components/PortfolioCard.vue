<template>
  <v-card class="my-3" hover>
    <v-card-media
        height="170px"
        :src="post.imgUrl">
    </v-card-media>
    <v-card-title primary-title>
        <div class="headline">{{ post.title }}</div>      
    </v-card-title>
    <v-card-text>
        {{ post.content }}
    </v-card-text>
    <v-card-actions>
        <v-tooltip bottom>
            <v-btn slot="activator" icon :href="post.githubUrl" target="_blank">
                <v-icon>fab fa-github</v-icon>
            </v-btn>
            <span>View On Github</span>
        </v-tooltip>
        <v-spacer></v-spacer>
        <v-btn flat class="blue--text" target="_blank" v-if="post.demoUrl && post.demoUrl.length > 0" :href="post.demoUrl">View Demo</v-btn>
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