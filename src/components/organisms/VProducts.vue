<template>
  <v-container grid-list-xl>
    <p class="text-xs-center headline">Products</p>
    <v-layout row wrap justify-space-around>
      <v-flex v-for="item in items" :key="item.name" xs12 sm6 md4 xl4>
        <v-card-list :item="item"></v-card-list>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
import VCardList from '~/components/molecules/VCardList'
export default {
  components: {
    VCardList
  },
  data() {
    return {
      items: [
        {
          name: 'Awesome Investor',
          src: require('~/assets/logo/awesome-investor.jpg'),
          discrib:
            'Internal management system of investment management company.',
          subItems: [
            {
              name: 'Feature',
              text:
                'We support comprehensively from investment judgment to execution, execution, and reporting. It can monitor the status of real-time positions and cash flows.It has all the necessary functions for the Investment manager.'
            },
            {
              name: 'Environ',
              text:
                'Frontend - Vue.js 2.7(Nuxt.js), Nuxt-Axios 1.0.0, Vuex Backend - Python 3.7 Django '
            }
          ],
          chips: [
            {
              color: 'yellow darken-1',
              text: 'Complete',
              textColor: ''
            },
            {
              color: 'grey',
              text: 'Private',
              textColor: 'white'
            }
          ]
        },
        {
          name: 'Cryptorage',
          src: require('~/assets/logo/arbitrage.jpg'),
          discrib: 'Crypto Asset Arbitrage Tool for Humansy.',
          subItems: [
            {
              name: 'Feature',
              text:
                'Provide real-time price acquisition and trade decision material.Support arbitrage trading between markets and currencies.'
            },
            {
              name: 'Environ',
              text: 'Frontend - Vue.js 2.8(Nuxt.js), Nuxt-Axios 1.0.0, Vuex'
            }
          ],
          chips: [
            {
              color: 'red',
              text: 'In Progress',
              textColor: 'white'
            },
            {
              color: 'blue',
              text: 'Public',
              textColor: 'white'
            }
          ],
          isLink: true,
          link: 'https://qiita.com/minoringo/items/917e325892733e0d606e'
        }
      ]
    }
  }
}
</script>

<style></style>
