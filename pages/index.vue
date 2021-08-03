<template>

  <v-card
    color="grey lighten-4"
    flat
    height="auto"
    tile
    class="main"
  >

    <v-container class="card--container" fluid>

      <!-- 首頁 -->
      <v-row id="home" dense>

        <v-img
          class="white--text align-center"
          src="/home/cindy__2.jpeg"
        >
          <span class="card--top--title">CINDY</span>
        </v-img>

      </v-row>

      <!-- 關於 -->
      <v-row id="about" dense>
        <v-col
          md="12"
          sm="12"
          xs="12"
        >
          <v-card-title class="card--title">
            <h2 class="text-center">關於Cindy</h2>
          </v-card-title>
        </v-col>

        <v-col
          md="6"
          sm="6"
          xs="12"
          style="padding-top: 0px;"
        >
          <v-img
            src="/about/cindy.jpeg"
          >
          </v-img>
        </v-col>

        <v-col
          md="6"
          sm="6"
          xs="12"
        >
          <div
            class="intro__block"
          >
            我是Cindy，牡羊座，理性又感性於一身<br>
            平時不把寫程式當成興趣的軟體工程師<br>
            卻享受寫程式遇到的各種挫折<br>
            不擅長與人聊天，但喜歡認識各行各業的人<br>
            近幾年迷戀上手作，特別是縫紉<br>
            不織布娃娃、棉布的各種小物<br>
            成為我工作之餘花最多時間的娛樂<br>
            人生終極目標是擁有自己的工作室<br>
            並且成為我賴以維生的工作<br>
            <br>
            從小受到父親耳濡目染<br>
            棒球成為我這輩子最了解的運動項目<br>
            沒有最支持的球隊<br>
            最欣賞的球員-味全龍曾陶鎔<br>
            <br>
            喜歡吃<br>
            不折不扣的小鳥胃吃貨<br>
            幫食物拍遺照也是興趣之一<br>
            <br>
            曾經想自彈自唱一首歌<br>
            但那是我大學加入吉他社時候的夢想<br>
            能彈不能唱，能唱不勿能彈<br>
            最後放棄了吉他<br>
            投入烏克麗麗的懷抱<br>
            也圓了自己其實熱愛音樂愛唱歌的夢<br>
            <br>
          </div>
        </v-col>
      </v-row>



      <!-- 生活 -->
      <v-row id="life" dense>
        <v-col
          md="12"
          sm="12"
          xs="12"
        >
          <v-card-title class="card--title">
            <h2 class="text-center">Cindy生活</h2>
          </v-card-title>
        </v-col>
      </v-row>

      <!-- 手作 -->
      <v-row>
        <v-col
          md="6"
          sm="6"
          xs="12"
          class="card--content"
        >
          <h1>手作・不織布・棉布</h1>
        </v-col>

        <v-col
          md="6"
          sm="6"
          xs="12"
        >
          <v-carousel
            hide-delimiters

            :interval="imageInterval"
            :height="imageHeight"
          >
            <v-carousel-item
              v-for="idx in 12"
              :key="idx"
              :src="`/handmade/Gadgelets__${idx}.jpeg`"
              :style="`width: ${imageWidth}px;`"
            ></v-carousel-item>
          </v-carousel>
        </v-col>
      </v-row>

      <!-- 棒球 -->
      <v-row>
        <v-col
          md="6"
          sm="6"
          xs="12"
        >
          <v-carousel
            hide-delimiters

            :interval="imageInterval"
            :height="imageHeight"
          >
            <v-carousel-item
              v-for="idx in 6"
              :key="idx"
              :src="`/baseball/Baseball__${idx}.jpeg`"
              :style="`width: ${imageWidth}px;`"
            ></v-carousel-item>
          </v-carousel>
        </v-col>

        <v-col
          md="6"
          sm="6"
          xs="12"
          class="card--content"
        >
          <h1>棒球</h1>
        </v-col>
      </v-row>

      <!-- 食物 -->
      <v-row>
        <v-col
          md="6"
          sm="6"
          xs="12"
          class="card--content"
        >
          <h1>食物・正餐・甜點</h1>
        </v-col>

        <v-col
          md="6"
          sm="6"
          xs="12"
        >
          <v-carousel
            hide-delimiters

            :interval="imageInterval"
            :height="imageHeight"
          >
            <v-carousel-item
              v-for="idx in 20"
              :key="idx"
              :src="`/food/Food__${idx}.jpeg`"
              :style="`width: ${imageWidth}px;`"
            ></v-carousel-item>
          </v-carousel>
        </v-col>

      </v-row>

    </v-container>

  </v-card>

</template>

<script>
export default {
  layout: 'default',

  data () {
    return {
      imageHeight: 'auto', // '542',
      imageWidth: 'auto', // '407',
      imageInterval: '1500'
    }
  },

  methods: {

  }

}
</script>

<style lang="scss">
.main {
  font-family: 'PingFangTC' !important;
}

.card {
  &--container {
    background-color: #ffffff !important;
  }

  &--top--title {
    font-family: 'PingFangTC' !important;
    font-size: 50px;
    font-weight: bold;
    letter-spacing: 5px;
    text-align: center;
    text-decoration: underline;
    display: block;
    color: rgba(255, 255, 255, 0.8);
  }

  &--title {
    font-family: 'PingFangTC' !important;
    display: block;
    padding: 20px 0px;
  }

  &--content {
    display: table;
  }
}

.row {
  background-color: #ffffff !important;
}

h1 {
  vertical-align: middle;
  display: table-cell;
  text-align: center;
  color: rgba(77, 77, 77, 0.8);
}

h2 {
  letter-spacing: 1px;
  color: rgb(95, 158, 160);
  padding: 70px 0 10px 0;
  border-bottom: 1px solid rgba(95, 158, 160, 0.2);
}

.intro__block {
  letter-spacing: 0.5px;
  padding: 0px 25px;
}
</style>