<template>
  <v-app>

    <!-- Header -->
    <Header/>

    <!-- Content -->
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>

    <!-- Footer -->
    <v-footer>
      <v-col
        cols="12"
        class="text-center"
      >
        Copyright <span style="vertical-align: middle;">&copy; {{ new Date().getFullYear() }}</span>
        Cindy Chao. All rights reserved.
      </v-col>
    </v-footer>
  </v-app>
</template>

<script>
import Header from '~/components/Header'

export default {
  components: {
    Header
  },

  data () {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  }
}
</script>
