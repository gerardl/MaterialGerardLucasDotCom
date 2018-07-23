<template>
  <v-app light>

    <v-content>
      <v-container class="main-container">
        <v-layout column wrap align-center>
          <v-flex xs12 md4>
            <portfolio-header />
          </v-flex>
          <v-flex xs12 md5>
            <div v-for="post in posts" :key="post.title">
              <portfolio-card :post="post"></portfolio-card>
            </div>
          </v-flex>   
        </v-layout>
      </v-container>
    </v-content>

    <portfolio-footer />
  </v-app>
</template>
<script>
import PortfolioHeader from './components/PortfolioHeader'
import PortfolioCard from './components/PortfolioCard'
import PortfolioFooter from './components/PortfolioFooter'

export default {
  name: 'App',
  components: {
    PortfolioHeader,
    PortfolioCard,
    PortfolioFooter
  },
  data () {
    return {
      title: 'Portfolio Home',
      // Will be creating a global api project to work with web api 2.
      // in-memory posts will move to this as soon as available.
      posts: [
          {
            title: 'Crypto-Ticker',
            content: 'I\'ve been engrossed in the .net world lately and only recently became aware of pusher, the hosted real time messaging platform.  I wanted to gain a little familiarity with it, so I used the existing bitstamp channels to create a mini crypto-tracking site.  I\'m not storing any values, so you will have to wait for the first trade to be made to see updated prices when you first load the page.',
            imgUrl: 'https://i.gyazo.com/15ae5b9164c60664b162b1547322aebe.png',
            githubUrl: 'https://github.com/gerardl/VuetifyTicker',
            demoUrl: 'http://ticker.gerardlucas.com'
          },
          {
            title: 'New Portfolio Site',
            content: 'Version 1 of the new site is live.  It uses Vuejs with the Vuetify material design framework.  Still tons I want to add, but so far happy with the progress!  It\'s not a template or anything, but feel free to use it for your own portfolio page.',
            imgUrl: 'https://i.gyazo.com/a0d2f569b93d730edbd860cc0ec83b06.png',
            githubUrl: 'https://github.com/gerardl/MaterialGerardLucasDotCom'
          },
          {
            title: 'Pooling Manager',
            content: 'One of the first issues I ran into when working with Unity3d was the cost of object creation.  Most games require tons of disposable objects for things like projectiles, spell effects, enemies and much more and Unity doesn\'t do much to help with caching these things or creating them before you need them.  This is a simple system to help fix some of these issues.  Pools of objects can be created and manipulated using C# code or the Unity editor.',
            imgUrl: 'https://camo.githubusercontent.com/af916419f95604cebcbd7ed8d3d1ec49f2cd70a5/687474703a2f2f692e696d6775722e636f6d2f465731657956442e6a7067',
            githubUrl: 'https://github.com/gerardl/PoolingManager'
          },
          {
            title: 'STL911',
            content: 'The city of St. Louis hosts up-to-date 911 call information on a public website.  This is a super handy thing to have, but when it first came out they were only displaying the last 20 or so calls.  To get around this, I created this .net project to scrape the site at a regular interval and store all calls in my own MS-SQL database for data analytics and mapping use.  This is obsolete and no longer in use as the city now releases tons of historical data with approximate geo-location for each call.',
            imgUrl: 'https://i.gyazo.com/296fe4475c1de86a7f715f2b2465eebe.png',
            githubUrl: 'https://github.com/gerardl/stl911'
          },
          {
            title: '2D RPG',
            content: 'One of my early forays into Unity3D game development.  This was a prototype project focusing on completing some of the main systems needed for a single player RPG.  I ended up implementing, stats, quests, enemies, equipment, aimed attacking and blocking, and much more in a top-down game world.',
            imgUrl: 'https://i.gyazo.com/e56b01e224a5aa94ef48ae824d53ad5e.png',
            githubUrl: 'https://github.com/gerardl/2DRPG',
            demoUrl: 'https://www.youtube.com/watch?v=2azM7cr6egc'
          },
          {
            title: 'Old Portfolio Site',
            content: 'This was the first website parked at gerardlucas.com.  It used an old bootstrap template with some simple modifications.',
            imgUrl: 'https://i.gyazo.com/db9309a4754174a2c384271282cbfc26.png',
            githubUrl: 'https://github.com/gerardl/GerardLucasDotCom',
            demoUrl: 'http://old.gerardlucas.com'
          }
        ]
    }
  }
}
</script>
<style>
 .main-container {
   max-width: 1200px;
 }
</style>
