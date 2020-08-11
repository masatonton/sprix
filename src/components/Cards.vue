<template>
  <v-card
    class="mx-auto"
    max-width="344"
  >
    <v-img
      src="../assets/coecuEgi.png"
      height="200px"
    ></v-img>

    <v-card-title>
      メソロギア
    </v-card-title>

    <v-card-subtitle>
      Vo1. Methologia Chapionship
    </v-card-subtitle>

    <v-card-actions>
      <v-btn text @click="twitterShare">Share</v-btn>

      <v-btn
        color="purple"
        text
      >
        エントリーページ
      </v-btn>

      <v-spacer></v-spacer>

      <v-btn
        icon
        @click="show = !show"
      >
        <v-icon>{{ show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
      </v-btn>
    </v-card-actions>

    <v-expand-transition>
      <div v-show="show">
        <v-divider></v-divider>

        <v-card-text>
          <h3>概要：</h3>
          <p>日程：9/?</p>
          <p>賞金<p/>
        </v-card-text>
      </div>
    </v-expand-transition>
  </v-card>
</template>

<script>
  export default {
    data: () => ({
      show: false,
    }),
    methods:{
      twitterShare(){
          //シェアする画面を設定
          var shareURL = 'https://twitter.com/intent/tweet?text=' + 'メソロギアの公式大会に参加しよう！！' + "%20%23メソロギア" + '&url=' + "ここに大会エントリーページのリンクを張ります";  
          //シェア用の画面へ移行
          location.href = shareURL
      }
    }
  }

  
</script>

