<template>
  <div>
    <p class="headline">Where I have been</p>

    <v-timeline>
      <v-timeline-item
        v-for="item in items"
        :key="item.title"
        :color="item.color"
        fill-dot
        small
      >
        <template v-slot:opposite>
          <span
            :class="`headline font-weight-bold ${item.color}--text`"
            v-text="item.year"
          ></span>
        </template>
        <v-card>
          <v-card-title :class="item.color">
            <h2 class="display-1 white--text font-weight-light">
              {{ item.title }}
            </h2>
          </v-card-title>
          <v-card-text>{{ item.text }}</v-card-text>
        </v-card>
      </v-timeline-item>
    </v-timeline>
  </div>
</template>

<script>
export default {
  data: () => ({
    items: [
      {
        year: 2019,
        color: 'cyan',
        title: 'What a new environment?',
        text: 'rsfjnaksfkajfkljfl ksjfkajlskafj jfsjalkfjaslfj'
      },
      {
        year: 2017,
        color: 'cyan',
        title: 'HC Asset Management co',
        text: 'rsfjnaksfkajfkljfl ksjfkajlskafj jfsjalkfjaslfj'
      },
      {
        year: 2013,
        color: 'cyan',
        title: 'University of Shizuoka',
        text:
          'The department is a department of business information, and majored in accounting.In particular, I studied mainly in corporate accounting, and obtained the 1st grade JBIC certificate, and in graduation thesis, I modeled the bankruptcy forecast of a company.'
      }
    ]
  })
}
</script>
