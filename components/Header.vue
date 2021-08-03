<template>
  <div style="height: 60px; padding: 0 20px;">
    <v-toolbar class="header" dense>
      <!-- <v-app-bar-nav-icon></v-app-bar-nav-icon> -->

      <!-- ToDo: 放Cindy文字圖片-->
      <v-toolbar-title>
        <a
          @click="scrollToTop()"
        >
          <b class="header--home">
            Cindy
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
        class="header--btn"
        href="https://www.instagram.com/cindy__handmade/"
        target="_blank"
      >
        <v-icon>mdi-instagram</v-icon>
      </v-btn>

    </v-toolbar>
  </div>

</template>

<script>
export default {

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
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 999;

  &--home {
    color: rgb(95, 158, 160);
    font-size: 25px;
    letter-spacing: 1px;
  }

  &--btn {
    width: 50px !important;
    margin: 10px;
  }
}

.v-toolbar__content {
  height: 60px !important;
}
</style>