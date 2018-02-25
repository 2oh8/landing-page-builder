<template>
  <div class="portfolio slideInUp">


    <div>
      <v-layout row wrap>
        <v-flex xs12 class="main-title-portfolio">
          <div class="svg-wrapper">
            <svg height="60" width="320" xmlns="http://www.w3.org/2000/svg">
              <rect class="shape" height="60" width="320" />
            </svg>
            <div class="text">PORTFOLIO</div>
          </div>
        </v-flex>

      </v-layout>

      </v-layout>
      <v-dialog v-model="dialogKanban" width="80%">
        <v-card class="info-dialog" style="z-index: 99 !important;">
          <v-card-title class="headline" style="font-family: Cinzel; z-index: 99 !important;">Vue Kanban</v-card-title>
          <iframe  style="z-index: 99 !important;" width="100%" class="video-iframe" src="https://www.youtube.com/embed/5eu15hzL1p4" frameborder="0" allowfullscreen></iframe>
          <v-card-title class="subtitle" style="font-family: Raleway; z-index: 99 !important;">A kanban board app used for making to-do lists. Users can add, organize and comment on different tasks, which are
            saved on the server for access anywhere, anytime.</v-card-title>
          <v-card-title class="subtitle" style="font-family: Raleway; z-index: 99 !important;">
            <v-icon style="z-index: 99 !important;">fa-github</v-icon>&nbsp;&nbsp;Contributors:&nbsp; <a style="color: #19f6e8" href="https://github.com/spencerhenze">Spencer Henze</a></v-card-title>
          <v-card-actions style="z-index: 99 !important;">
            <v-spacer></v-spacer>
            <v-btn class="close-dialog-button" flat="flat" @click.native="dialogKanban = false" style="font-family: Raleway; z-index: 99 !important;">Close</v-btn>
          </v-card-actions>
        </v-card>
      </v-dialog>

      <v-dialog v-model="dialogGetmusic" width="80%">
        <v-card class="info-dialog">
          <v-card-title class="headline" style="font-family: Cinzel">get.music</v-card-title>
          <iframe width="100%" class="video-iframe" src="https://www.youtube.com/embed/oLh70_dERzg" frameborder="0" allowfullscreen></iframe>
          <v-card-title class="subtitle" style="font-family: Raleway">Simple app that allows users to search and sample music using the iTunes API.</v-card-title>
          <v-card-actions>
            <v-spacer></v-spacer>
            <v-btn class="close-dialog-button" flat="flat" @click.native="dialogGetmusic = false" style="font-family: Raleway">Close</v-btn>
          </v-card-actions>
        </v-card>
      </v-dialog>

      <v-dialog v-model="dialogGridgames" width="80%">
        <v-card class="info-dialog">
          <v-card-title class="headline" style="font-family: Cinzel">Gridworks Games</v-card-title>
          <iframe width="100%" class="video-iframe" src="https://www.youtube.com/embed/p-ymo5NARZo" frameborder="0" allowfullscreen></iframe>
          <v-card-title class="subtitle" style="font-family: Raleway">A mobile-responsive gaming platform where other game developers can plug in their own games that communicate player
            stats to a persistent leaderboard and ranking system.</v-card-title>
          <v-card-title class="subtitle" style="font-family: Raleway">
            <v-icon>fa-github</v-icon>&nbsp;&nbsp;Contributors:&nbsp; <a style="color: #19f6e8" href="https://github.com/deannafoster">DeAnna Foster</a>&nbsp;
            <a style="color: #19f6e8" href="https://github.com/acaroselli1">Alex Caroselli</a>&nbsp;<a style="color: #19f6e8"
              href="https://github.com/werewolfred">Austin Harn</a> &nbsp;
            <a style="color: #19f6e8" href="https://github.com/cammackj">Josh Cammack</a>
          </v-card-title>
          <v-card-actions>
            <v-spacer></v-spacer>
            <v-btn class="close-dialog-button" flat="flat" @click.native="dialogGridgames = false" style="font-family: Raleway">Close</v-btn>
          </v-card-actions>
        </v-card>
      </v-dialog>

      <v-dialog v-model="dialogAfterhrs" width="80%">
        <v-card class="info-dialog">
          <v-card-title class="headline" style="font-family: Cinzel">Afterhrs (in Beta Testing)</v-card-title>
          <iframe width="100%" class="video-iframe" src="https://www.youtube.com/embed/8V5d16-6i9g" frameborder="0" allowfullscreen></iframe>
          <v-card-title class="subtitle" style="font-family: Raleway">A social media app where users 21+ can chat with friends, share favorite bars and drinks, and user location-based
            services to meet up with one another. Incorporates several APIs, including the Absolut Drinks Database.</v-card-title>
          <v-card-actions>
            <v-spacer></v-spacer>
            <v-btn class="close-dialog-button" flat="flat" @click.native="dialogAfterhrs = false" style="font-family: Raleway">Close</v-btn>
          </v-card-actions>
        </v-card>
      </v-dialog>

      <v-dialog v-model="dialogJelliKeepr" width="80%">
        <v-card class="info-dialog">
          <v-card-title class="headline" style="font-family: Cinzel">JelliKeepr</v-card-title>
          <iframe width="100%" class="video-iframe" src="https://www.youtube.com/embed/WuevMHtB1gs" frameborder="0" allowfullscreen></iframe>
          <v-card-title class="subtitle" style="font-family: Raleway">A different take on pinterest, JelliKeepr allows users to post and store "keeps" to publicly or to different vaults.
            The twist? The vaults and their contents are surounded by responsive gooey jelly! Made with Vue.js 2.0, Vuetify.js,
            and some fun canvas effects found on CodePen.</v-card-title>
          <v-card-actions>
            <v-spacer></v-spacer>
            <v-btn class="close-dialog-button" flat="flat" @click.native="dialogJelliKeepr = false" style="font-family: Raleway">Close</v-btn>
          </v-card-actions>
        </v-card>
      </v-dialog>

      <v-dialog v-model="dialogPlau" width="80%">
        <v-card class="info-dialog">
          <v-card-title class="headline" style="font-family: Cinzel">Plaü (in Beta Testing)</v-card-title>
          <iframe width="100%" class="video-iframe" src="https://www.youtube.com/embed/XBM4_eStLrw" frameborder="0" allowfullscreen></iframe>
          <v-card-title class="subtitle" style="font-family: Raleway">An on-demand snow-plow app inspired by one of the harshest winters Idaho has ever seen. Plaü allows users (and
            their neighbors) to place bids on their street. The higher the bid, the greater the demand for snow plow drivers
            to come and collect the bounty. Implements Google Maps API and location based services.</v-card-title>
          <v-card-actions>
            <v-spacer></v-spacer>
            <v-btn class="close-dialog-button" flat="flat" @click.native="dialogPlau = false" style="font-family: Raleway">Close</v-btn>
          </v-card-actions>
        </v-card>
      </v-dialog>

      <v-layout column class="gallery-row">
        <div class="info-card-gallery">
          <div class="info-card info-card-index6">

            <div class="info-card__overlay">
              <h2 class="info-card__title">JelliKeepr</h2>
              <a class="info-card__subcontent" href="https://jellikeepr.herokuapp.com/">Demo <i class="icon-eye"></i></a>
              <a class="info-card__subcontent" href="https://github.com/2oh8/keepr-node">Code <i class="fa fa-code" aria-hidden="true"></i></a>
              <a class="info-card__subcontent" @click.stop="openJelliKeepr">About <i class="fa fa-info" aria-hidden="true"></i></a>
            </div>
          </div>

          <div class="info-card info-card-index7">

            <div class="info-card__overlay">
              <h2 class="info-card__title">Plaü</h2>
              <a class="info-card__subcontent" href="https://plau.herokuapp.com/">Demo <i class="icon-eye"></i></a>
              <a class="info-card__subcontent" href="https://github.com/2oh8/plau">Code <i class="fa fa-code" aria-hidden="true"></i></a>
              <a class="info-card__subcontent" @click.stop="openPlau">About <i class="fa fa-info" aria-hidden="true"></i></a>
            </div>
          </div>

          <div class="info-card info-card-index5">

            <div class="info-card__overlay">
              <h2 class="info-card__title">afterhrs</h2>
              <a class="info-card__subcontent" href="https://afterhrs.herokuapp.com/">Demo <i class="icon-eye"></i></a>
              <a class="info-card__subcontent" href="https://github.com/2oh8/afterhrs">Code <i class="fa fa-code" aria-hidden="true"></i></a>
              <a class="info-card__subcontent" @click.stop="openAfterhrs">About <i class="fa fa-info" aria-hidden="true"></i></a>
            </div>
          </div>
          <div class="info-card info-card-index1">

            <div class="info-card__overlay">
              <h2 class="info-card__title">Vue Kanban</h2>
              <a class="info-card__subcontent" href="https://zen-kanban.herokuapp.com/">Demo <i class="icon-eye"></i></a>
              <a class="info-card__subcontent" href="https://github.com/2oh8/vue-kanban">Code <i class="fa fa-code" aria-hidden="true"></i></a>
              <a class="info-card__subcontent" @click.stop="openKanban">About <i class="fa fa-info" aria-hidden="true"></i></a>
            </div>
          </div>

          <div class="info-card info-card-index4">

            <div class="info-card__overlay">
              <h2 class="info-card__title">Gridworks Games</h2>
              <a class="info-card__subcontent" href="https://gridgames.herokuapp.com/">Demo <i class="icon-eye"></i></a>
              <a class="info-card__subcontent" href="https://github.com/2oh8/gridworks-games">Code <i class="fa fa-code" aria-hidden="true"></i></a>
              <a class="info-card__subcontent" @click.stop="openGridgames">About <i class="fa fa-info" aria-hidden="true"></i></a>
            </div>
          </div>

          <div class="info-card info-card-index2">

            <div class="info-card__overlay">
              <h2 class="info-card__title">get.music</h2>
              <a class="info-card__subcontent" href="https://2oh8.github.io/Music-Is-Fun/">Demo <i class="icon-eye"></i></a>
              <a class="info-card__subcontent" href="https://github.com/2oh8/Music-Is-Fun">Code <i class="fa fa-code" aria-hidden="true"></i></a>
              <a class="info-card__subcontent" @click.stop="openGetmusic">About <i class="fa fa-info" aria-hidden="true"></i></a>
            </div>
          </div>

          <div class="info-card info-card-index3">

            <div class="info-card__overlay">
              <h2 class="info-card__title">Inspire</h2>
              <a class="info-card__subcontent" href="https://github.com/2oh8/Inspire-Project">Code <i class="fa fa-code" aria-hidden="true"></i></a>
            </div>
          </div>





        </div>
      </v-layout>


    </div>


  </div>
  </div>

</template>

<script>
  export default {
    name: 'portfolio',
    mounted() {
      // window.sr = ScrollReveal({ duration: 2000 });
      // sr.reveal('.main-title-portfolio');
      // sr.reveal('.main-subtitle-portfolio');
      // sr.reveal('.gallery-row');
    },
    data() {
      return {
        dialogKanban: false,
        dialogGetmusic: false,
        dialogGridgames: false,
        dialogAfterhrs: false,
        dialogJelliKeepr: false,
        dialogPlau: false
      }
    },
    methods: {
      openKanban() {
        this.dialogKanban = true
      },
      openGetmusic() {
        this.dialogGetmusic = true
      },
      openGridgames() {
        this.dialogGridgames = true
      },
      openAfterhrs() {
        this.dialogAfterhrs = true
      },
      openJelliKeepr() {
        this.dialogJelliKeepr = true
      },
      openPlau() {
        this.dialogPlau = true
      }
    }
  }

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  /* .main-title-portfolio {
    margin-top: 3vh;
  } */

  .video-iframe {
    height: 55vh;
  }

  .info-dialog {
    background: rgba(66, 66, 66, .75);
    z-index: 99 !important;
  }

  .close-dialog-button {
    color: #19f6e8;
  }

  .main-subtitle-portfolio {
    color: white;
    text-align: center;
    font-family: 'Cinzel';
    letter-spacing: 3px;
  }

  .gallery-row {
    height: 25rem !important;
  }

  @media(max-width: 768px) {
    .gallery-row {
      height: 70rem !important;
    }
  }

  .gallery-row:last-of-type {
    height: auto !important;
  }

  .svg-wrapper {
    text-align: center;
    position: relative;
    top: 50%;
    transform: translateY(-50%);
    margin: 0 auto;
    width: 320px;
    height: 70px;
  }

  .shape {
    stroke-dasharray: 140 540;
    stroke-dashoffset: -474;
    stroke-width: 8px;
    fill: transparent;
    stroke: #19f6e8;
    border-bottom: 5px solid black;
    transition: stroke-width 1s, stroke-dashoffset 1s, stroke-dasharray 1s;
  }

  .text {
    font-family: 'Cinzel';
    font-size: 22px;
    line-height: 32px;
    letter-spacing: 8px;
    color: #fff;
    top: -48px;
    position: relative;
  }

  .svg-wrapper:hover .shape {
    stroke-width: 2px;
    stroke-dashoffset: 0;
    stroke-dasharray: 760;
  }
</style>