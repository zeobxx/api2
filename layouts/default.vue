<template>
  <v-app>
    <v-app-bar :clipped-left="clipped" fixed app>
      <v-toolbar-title text-align: center v-text="title" />
      <v-spacer />
    </v-app-bar>
    <v-main>
      <v-container fluid>
        <nuxt />
      </v-container>
    </v-main>
    <v-footer :absolute="!fixed" app>
      @ jikin Api
    </v-footer>
      <v-carousel hide-delimiters>
    <v-carousel-item
      v-for="(item,i) in items"
      :key="i"
      :src="item.src"
    ></v-carousel-item>
  </v-carousel>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      clipped: false,
      fixed: false,
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'ZEOBX_MANGA',
      items: [
          {
            src: 'https://i.pinimg.com/originals/53/8b/17/538b1769089f5604920570920e50eb50.jpg',
          },
          {
            src: 'https://i.pinimg.com/originals/fd/67/63/fd6763c75d1dbc9a1c88e9498b8ef4df.jpg',
          },
          {
            src: 'https://www.tkpark.or.th/stocks/extra/0061e8.jpg',
          },
        ],
    }
  },
}
</script>