<template>
  <div style="height: 60px;">
    <v-toolbar class="header" dense>
      <!-- <v-app-bar-nav-icon></v-app-bar-nav-icon> -->

      <v-toolbar-title>
        <a
          @click="scrollToTop()"
        >
          <b class="header--home">
            <v-img :src="homeIcon" height="60" width="60"></v-img>
          </b>
        </a>
      </v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn
        icon
        class="header--btn"
        @click="scrollToTop()"
      >
        <!-- <v-icon>mdi-home</v-icon> -->
        首頁
      </v-btn>

      <v-btn
        icon
        class="header--btn"
        v-scroll-to="'#about'"
      >
        <!-- <v-icon>mdi-account</v-icon> -->
        關於
      </v-btn>

      <v-btn
        icon
        class="header--btn"
        v-scroll-to="'#life'"
      >
        <!-- <v-icon>mdi-image</v-icon> -->
        生活
      </v-btn>

      <v-btn
        icon
        class="header--link"
        href="https://www.instagram.com/cindy__handmade/"
        target="_blank"
      >
        <v-icon>mdi-instagram</v-icon>
      </v-btn>

      <v-btn
        icon
        class="header--link"
        href="https://twitter.com/Cindy__Chao"
        target="_blank"
      >
        <v-icon>mdi-twitter</v-icon>
      </v-btn>

      <v-btn
        icon
        class="header--link"
        href="https://github.com/CindyChaoHY"
        target="_blank"
      >
        <v-icon>mdi-github</v-icon>
      </v-btn>

    </v-toolbar>
  </div>

</template>

<script>
export default {
  data () {
    return {
      homeIcon: require('@/assets/img/cindy_icon.jpg')
    }
  },

  methods: {
    scrollToTop() {
      window.scrollTo({
        top: 0,
        left: 0,
        behavior: 'smooth'
      })
    }
  }

}
</script>

<style lang="scss">
.header {
  height: 60px !important;
  position: fixed !important;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 999;
  background: rgba(148, 229, 210, 0.2) !important;

  &--home {
    color: rgb(95, 158, 160);
    font-size: 25px;
    letter-spacing: 1px;
  }

  &--btn {
    width: 50px !important;
    margin: 10px;
  }

  &--link {
    width: 40px !important;
    margin: 0px !important;
  }
}

.v-toolbar__content {
  height: 60px !important;
  padding: 0px 16px 0px 0px !important;
}

@media (max-width: 600px) {
  .header--btn {
    width: 40px !important;
    margin: 5px;
  }

  .header--link {
    width: 30px !important;
    margin: 0px;
  }
}
</style>