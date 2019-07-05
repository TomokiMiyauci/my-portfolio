<template>
  <v-container>
    <v-layout>
      <v-flex>
        <v-card flat class="elevation-0 transparent">
          <v-card-title>
            <div class="headline">Contact Me</div>
          </v-card-title>
          <v-card-text
            >If you are interested in me, please contact me.</v-card-text
          >
          <v-list class="transparent">
            <v-list-item v-for="item in items" :key="item.icon">
              <v-list-item-action>
                <v-icon class="red--text">{{ item.icon }}</v-icon>
              </v-list-item-action>
              <v-list-item-content>
                <v-list-item-title>{{ item.text }}</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    items: [
      { icon: 'person', text: 'Tomoki Miyauchi' },
      { icon: 'place', text: 'Tokyo, JA' },
      { icon: 'email', text: 'development.operation.6.6.6@gmail.com' }
    ]
  })
}
</script>

<style></style>
