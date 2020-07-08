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
      <v-btn text>SHARE</v-btn>

      <v-btn
        color="purple"
        text
      >
        詳細/エントリーページ
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
          <p>日程：8/2</p>
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
  }

  
</script>

