<template>
  <v-container>
    <p class="headline">Where I have been</p>

    <v-timeline dense align-top>
      <v-timeline-item
        v-for="item in items"
        :key="item.title"
        :color="item.color"
        fill-dot
        small
      >
        <v-layout pt-3>
          <v-flex xs2 xl1>
            <span>{{ item.year }}</span>
          </v-flex>
          <v-flex>
            <v-card>
              <v-card-title :class="item.color">
                <h2 class="display-1 white--text font-weight-light">
                  {{ item.title }}
                </h2>
              </v-card-title>
              <v-card-text>{{ item.text }}</v-card-text>
            </v-card>
          </v-flex>
        </v-layout>
      </v-timeline-item>
    </v-timeline>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    items: [
      {
        year: 2019,
        color: 'red',
        title: 'What a new environment?',
        text:
          'I was impressed by the culture of the OSS and decided to stay in the IT industry. I am looking forward new job.'
      },
      {
        year: 2017,
        color: 'grey',
        title: 'HC Asset Management Co., Ltd.',
        text:
          'HC Asset is an investment management company that mainly manages corporate pension funds and credit unions.　In particular, we deal with LPS products, which have special schemes and management methods and are very niche. I joined this company in 2017.'
      },
      {
        year: 2013,
        color: 'grey',
        title: 'University of Shizuoka',
        text:
          'The department is a department of business information, and majored in accounting.In particular, I studied mainly in corporate accounting, and obtained the 1st grade JBIC certificate, and in graduation thesis, I modeled the bankruptcy forecast of a company.'
      }
    ]
  })
}
</script>
