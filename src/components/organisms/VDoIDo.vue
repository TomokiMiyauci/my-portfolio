<template>
  <v-container grid-list-xl>
    <h1 class="headline">What do I in HC</h1>

    <v-layout row wrap>
      <v-flex v-for="item in items" :key="item.title" xs12 sm6 md4 xl4>
        <v-card>
          <v-card-title primary-title :class="item.color">
            <div class="headline white--text">{{ item.title }}</div>
          </v-card-title>
          <v-card-text>
            <span class="subheading grey--text">{{ item.subTitle }}</span>
            <!-- eslint-disable-next-line -->
            <span v-html="item.text">{{ item.text }}</span>
          </v-card-text>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    items: [
      {
        color: 'blue',
        title: 'Back Office',
        subTitle: '2017 - Now',
        text: `<ul>
        <li>Responsiblefor overall contract processing for foreign nationals and domestic registered investment trusts</li>
        <li>We are in charge of general duties about call business / distribution correspondence, mark-to-market, cash management from investment business limited liability union application -Preparation of operation report, report</li>
        <li>Fund's foreign exchange, Japanese yen input processing</li>
        <li>System entry and management of settlement account information</li>
        <li>Delivery of funds, general check business</li>
        <li>Commitment communication with re-trust bank</li>
        <li>Other department internal business operations (Making of meeting materials, telephone calls, guidance of junior staff, temporary staff, etc.)</li>
        <li>Proposal of efficiency improvement proposal of business input work using Access tool and creation of business manual</li>
        </ul> `
      },
      {
        color: 'blue',

        title: 'Front Office',
        subTitle: '2018 - Now',
        text: `<ul>
        <li>Execution of fund trading, preparation for real exchange rate</li>
        <li>Hedge ratio management in hedge account, Role enforcement, Prepare for the actual demand exchange on call and distribution in investment business limited liability union</li></ul>`
      },
      {
        color: 'red',
        title: 'Development',
        subTitle: '2018 - Now',
        text: `<ul>
        <li>Internal system environment (Web App) construction plan, Requirements definition, Basic design, Coding, Unit test, Comprehensive test</li>
        <li>Development of Single Page Application with Vue.js (Nuxt.js) as the front end and Dango Rest Framework as the back end.</li>
        <li>Migration from existing Access-based backbone systems to browser-based internal systems.</li>
        <li>Implementation of uniform management using DB from a system in which Excel was the dominant management tool.</li></ul>`
      }
    ]
  })
}
</script>

<style></style>
