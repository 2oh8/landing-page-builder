<template>
  <div class="home slideInUp">


    <div>
      <v-layout row wrap>
        <v-flex xs12 class="main-title-home">
          <div class="svg-wrapper">
            <svg height="60" width="320" xmlns="http://www.w3.org/2000/svg">
              <rect class="shape" height="60" width="320" />
            </svg>
            <div class="text">MATT YOUNG</div>
          </div>
        </v-flex>
        <v-flex xs12>
          <p class="main-subtitle-home">FULL STACK WEB DEVELOPMENT</p>
        </v-flex>

      </v-layout>


      <v-layout row class="home-gallery">

        <!-- <img style="opacity: .95" src="http://ghchart.rshah.org/2oh8" alt="Github Contributions within the last year." /> -->



        <div class="info-card info-card-index3-home">

          <div class="info-card__overlay">
            <h2 class="info-card__title">Resume</h2>
            <a class="info-card__subcontent"style="text-decoration: none !important;"href="https://www.dropbox.com/s/nth5lb6lewp28z3/Matt%20Young%20-%20Web%20Development%20Resume.pdf?dl=0">Learn more about me.</a>
          </div>
        </div>

        <div class="info-card info-card-index1-home">

          <div class="info-card__overlay">
            <h2 class="info-card__title">Portfolio</h2>
            <router-link class="info-card__subcontent" to="/Portfolio">Check out my work.</router-link>
          </div>
        </div>




      </v-layout>



    </div>


  </div>
</template>

<script>
  export default {
    name: 'home',
    mounted() {
      // window.sr = ScrollReveal({ duration: 2000 });
      // sr.reveal('.main-title-home');
      // sr.reveal('.main-subtitle-home');
      // sr.reveal('.home-gallery');


    },
    data() {
      return {

      }
    }
  }

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .main-title-home {
    /* margin-top: 1vh; */
  }

  .main-subtitle-home {
    color: white;
    text-align: center;
    font-family: 'Cinzel';
    letter-spacing: 3px;
  }

  .info-card-gallery {
    width: 100% !important;
  }
  .home {
    width: 100%;
  }

  .home-gallery {
    margin-top: 50px;
    width: auto;
    height: auto;
    margin: 50px auto;
    max-width: 100%;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    flex: 1 1 auto;
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