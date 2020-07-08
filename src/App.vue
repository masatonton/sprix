<template>
  <v-app>
        <v-navigation-drawer app v-model="drawer">
      <v-list-item>
        <v-list-item-title class="title">
          Sprix
        </v-list-item-title>
        <v-btn icon>
          <v-icon>mdi-chevron-left</v-icon>
        </v-btn>
      </v-list-item>
      <v-divider />
      <v-list nav>
        <v-list-item v-for="menu in menus" :key="menu.title" :to="menu.url">
          <v-list-item-icon>
            <v-icon>{{ menu.icon }}</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title>{{ menu.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar app dark>
      <!-- アプリケーションバー -->
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-toolbar-title>Sprix</v-toolbar-title>
    </v-app-bar>

    <v-content>
      <Navigation/>
      <Carousels/> <br><br><br>
      <h2>Events</h2><br>
      <Cards/> <br>
      <Cards2/><br><br>
      <v-divider></v-divider> <br><br>
      <h2 style="" >About Sprix</h2><br>
      <Footer/>
    </v-content>
  </v-app>
</template>

<script>

import Carousels from './components/Carousels';
import Cards from './components/Cards';
import Cards2 from './components/Cards2';
import Footer from './components/Footer';

export default {
  name: 'App',

  components: {
    Carousels,
    Cards,
    Cards2,
    Footer,
  },

    data: () => ({
    drawer: false,
    menus: [
      { title: 'Event', icon: 'mdi-web', url: '#events' },
      { title: 'About', icon: 'mdi-home', url: '#about' },
      { title: 'How to Entry', icon: 'mdi-heart', url: '#How' },
      { title: 'Contact', icon: 'mdi-information-variant', url:'#contact'}
    ]
  })
} 
  
</script>

<style scoped>
</style>>