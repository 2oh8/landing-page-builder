<template>

  <v-app class="main-app-background" dark>
    <v-navigation-drawer class="main-navigation-drawer" persistent :mini-variant="miniVariant" v-model="drawer" enable-resize-watcher>
      <v-list class="navigation-icon">
        <v-list-tile>
          <v-list-tile-action>
            <router-link to="/">
              <v-icon dark style="font-family: Cinzel" class="menu-icon">M</v-icon>
            </router-link>
          </v-list-tile-action>
        </v-list-tile>
        <v-list-tile>
          <v-list-tile-action>
            <router-link to="/Portfolio">
              <i class="fa fa-code menu-icon"></i>
            </router-link>
          </v-list-tile-action>
        </v-list-tile>
        <v-list-tile>
          <router-link to="/Resume">
            <v-list-tile-action>
              <i class="fa fa-file-pdf-o menu-icon"></i>
            </v-list-tile-action>
          </router-link>
        </v-list-tile>
        <v-list-tile>
          <a href="https://www.github.com/2oh8/">
            <v-list-tile-action>
              <i class="fa fa-github menu-icon"></i>
            </v-list-tile-action>
          </a>
        </v-list-tile>
        <v-list-tile>
          <a href="https://www.linkedin.com/in/matt-young-a299a076">
            <v-list-tile-action>
              <i class="fa fa-linkedin menu-icon"></i>
            </v-list-tile-action>
          </a>
        </v-list-tile>
        <v-list-tile>
          <a href="mailto:matthewdyoung@att.net">
            <v-list-tile-action>
              <i class="fa fa-paper-plane menu-icon"></i>
            </v-list-tile-action>
          </a>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
    <v-toolbar class="main-toolbar" fixed>

      <div class="navigation-hamburger">
        <div id="nav-icon1" v-bind:class="{ open: drawer }" @click.stop="drawer = !drawer">
          <span></span>
          <span></span>
          <span></span>
        </div>
      </div>

      <!-- <v-toolbar-title v-text="title"></v-toolbar-title> -->
      <v-spacer></v-spacer>
    </v-toolbar>
    <main>
      <v-container fluid>
        <v-slide-y-transition mode="out-in">
          <v-layout column align-center>

            <!-- ROUTER VIEW -->
            <router-view></router-view>
            <!-- ROUTER VIEW -->

          </v-layout>
        </v-slide-y-transition>
      </v-container>
    </main>

    <v-snackbar :timeout="timeout" :top="y === 'top'" :bottom="y === 'bottom'" :right="x === 'right'" :left="x === 'left'" :multi-line="mode === 'multi-line'"
      :vertical="mode === 'vertical'" v-model="snackbar" class="snackbar-message elevation-24">
      {{ text }}
    </v-snackbar>
  </v-app>
</template>
<script>
  export default {
    mounted() {
      this.snackbar = true;
      // sr.reveal('.navigation-hamburger');
      // sr.reveal('.menu-icon');
      // sr.reveal('.navigation-icon');
    },
    data() {
      return {
        // SNACKBAR //
        snackbar: false,
        y: 'bottom',
        x: null,
        mode: 'vertical',
        timeout: 6000,
        text: 'Use chat to contact me directly at any time during your visit.',
        // END SNACKBAR //
        drawer: false,
        fixed: false,
        miniVariant: true,
        right: true,
        title: 'Vuetify.js'
      }
    }
  }

</script>
<style>
  @keyframes slideInUp {
    from {
      transform: translate3d(0, 100%, 0);
      visibility: visible;
    }
  
    to {
      transform: translate3d(0, 0, 0);
    }
  }
  
  .slideInUp {
    animation-name: slideInUp;
    animation-timing-function: ease;
    animation-duration: 2s;
  }
</style>
<style scoped>
  * {
    text-decoration: none !important;
  }


  .snackbar-message {
    background: rgba(25, 246, 232, .35) !important;
    color: black !important;
    font-family: 'Raleway' !important;
  }

  .menu-icon {
    font-size: 1.5rem;
  }

  .main-app-background {
    background: url('./assets/background.png') !important;
  }

  .main-toolbar {
    background: linear-gradient(rgba(0, 0, 0, .5), rgba(0, 0, 0, 0)) !important;
    box-shadow: none !important;
  }

  .main-navigation-drawer {
    background: transparent !important;
    box-shadow: none !important;
    border: none !important;
  }

  .navigation-icon {
    background: transparent !important;
  }

  .navigation-hamburger {
    left: 0 !important;
    margin-top: 2rem !important;
    margin-left: 2rem !important;
  }
  /* ANIMATED HAMBURGER FOR NAV */
  /* Icon 1 */

  #nav-icon1,
  #nav-icon2,
  #nav-icon3,
  #nav-icon4 {
    width: 60px;
    height: 45px;
    position: relative;
    margin: 50px auto;
    -webkit-transform: rotate(0deg);
    -moz-transform: rotate(0deg);
    -o-transform: rotate(0deg);
    transform: rotate(0deg);
    -webkit-transition: .5s ease-in-out;
    -moz-transition: .5s ease-in-out;
    -o-transition: .5s ease-in-out;
    transition: .5s ease-in-out;
    cursor: pointer;
  }

  #nav-icon1 span,
  #nav-icon3 span,
  #nav-icon4 span {
    display: block;
    position: absolute;
    height: 3px;
    width: 50%;
    background: white;
    border-radius: 3px;
    opacity: 1;
    /* left: 0; */
    -webkit-transform: rotate(0deg);
    -moz-transform: rotate(0deg);
    -o-transform: rotate(0deg);
    transform: rotate(0deg);
    -webkit-transition: .25s ease-in-out;
    -moz-transition: .25s ease-in-out;
    -o-transition: .25s ease-in-out;
    transition: .25s ease-in-out;
  }

  #nav-icon1 span:nth-child(1) {
    top: 0vh;
  }

  #nav-icon1 span:nth-child(2) {
    top: 1vh;
  }

  #nav-icon1 span:nth-child(3) {
    top: 2vh;
  }

  #nav-icon1.open span:nth-child(1) {
    top: 1vh;
    -webkit-transform: rotate(135deg);
    -moz-transform: rotate(135deg);
    -o-transform: rotate(135deg);
    transform: rotate(135deg);
  }

  #nav-icon1.open span:nth-child(2) {
    opacity: 0;
    left: -60px;
  }

  #nav-icon1.open span:nth-child(3) {
    top: 1vh;
    -webkit-transform: rotate(-135deg);
    -moz-transform: rotate(-135deg);
    -o-transform: rotate(-135deg);
    transform: rotate(-135deg);
  }
</style>
<style lang="stylus">
  @import './stylus/main'
</style>