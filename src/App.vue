<template>
  <v-app>
    <v-app-bar app dark>
      <!-- アプリケーションバー -->
      <v-toolbar-title style="margin-left:4vw;">
        <div>
        <v-img class="logo"
          src="./assets/sprixlogo.png"
        ></v-img>
        </div>
      </v-toolbar-title>
      
      <v-spacer></v-spacer>

    
      <v-btn  icon style="margin-right:4vw;" href="https://twitter.com/messages/compose?recipient_id=951155124646305792">
        <v-icon large color="orange darken-2">mdi-email</v-icon>
      </v-btn>
      
    </v-app-bar>

    <v-content>
      <Navigation/>
      <Carousels/><br><br>
      <v-card  class="d-flex pa-2 subtitle" id="0">
      <h2 class="maintitle">イベント</h2>
      </v-card><br>
      <Cards/><br><br>
      <v-card  class="d-flex pa-2 subtitle"  id="2">
      <h2 class="maintitle">大会の流れ</h2>
      </v-card><br><br>
      <Smalldots/><br><br>
      <br><br>
      <v-card  class="d-flex pa-2 subtitle"  id="3">
      <h2 class="maintitle">大会結果</h2>
      </v-card><br><br>
      <Table/>
      <v-divider></v-divider> <br><br>
      <Team/><br><br>
      <Footer/>
    </v-content>
  </v-app>
</template>

<script>

import Carousels from './components/Carousels';
import Cards from './components/Cards';
// import Cards2 from './components/Cards2';
import Footer from './components/Footer';
import Smalldots from './components/Smalldots'
import Table from './components/Table'
import Team from './components/Team'

export default {
  name: 'App',

  components: {
    Carousels,
    Cards,
   // Cards2,
    Footer,
    Smalldots,
    Table,
    Team,
  },

    data: () => ({
    drawer: false,
    menus: [
      { title: 'イベント', icon: 'mdi-web', url: "#0" },
      { title: '運営', icon: 'mdi-home', url:  "#1" },
      { title: '大会の流れ', icon: 'mdi-heart', url:  "#2" },
      { title: '過去の大会結果', icon: 'mdi-information-variant', url: "#3"}
    ]
  })
} 
  
</script>

<style scoped>
.subtitle{
  margin: 0vw 5vw;
  background-color:rgb(207, 8, 141);
}

.maintitle{
  color:white;
  margin-left: 5vw;
}

.logo{
  max-width:120px; /* 画像の最大幅 */
  margin: auto; /* 画像の左右の余白を同じ幅にする */
  display: block; /* 画像の下の隙間をなくす */
}

</style>