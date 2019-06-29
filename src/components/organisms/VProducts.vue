<template>
  <v-container grid-list-xs>
    <p class="text-xs-center headline">- Products -</p>
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
            'Internal management system of investment management company',
          subItems: [
            { name: 'Feature', text: 'Lorem' },
            { name: 'Environ', text: 'Frontend - Python' }
          ]
        },
        {
          name: 'Cryptorage',
          src: require('~/assets/logo/arbitrage.jpg'),
          discrib:
            'Internal management system of investment management company',
          subItems: [
            { name: 'Feature', text: 'Lorem' },
            { name: 'Environ', text: 'Frontend - Python' }
          ]
        }
      ]
    }
  }
}
</script>

<style></style>
