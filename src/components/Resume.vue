<template>
  <div class="resume">

    <v-layout row wrap>
      <v-flex xs12 class="main-title">
        <div class="svg-wrapper">
          <svg height="60" width="320" xmlns="http://www.w3.org/2000/svg">
            <rect class="shape" height="60" width="320" />
          </svg>
          <div class="text">RÉSUMÉ</div>
        </div>
      </v-flex>
      <v-flex xs12>
        <p class="main-subtitle">GET A COPY <a style="text-decoration: none !important;" href="https://www.linkedin.com/in/matt-young-a299a076"><v-icon>fa-linkedin</v-icon></a> <a style="text-decoration: none !important;"href="https://www.dropbox.com/s/nth5lb6lewp28z3/Matt%20Young%20-%20Web%20Development%20Resume.pdf?dl=0"><v-icon>fa-download</v-icon></a></p>
      </v-flex>
    </v-layout>

    <ul class="timeline">
      <!-- Item 1 -->
      <li>
        <div class="direction-r">
          <div class="flag-wrapper">
            <span class="hexa"></span>
            <span class="flag">Office Depot</span>
            <span class="time-wrapper"><span class="time">OCT 2011</span></span>
          </div>
          <div class="desc">Aside from the day-to-day upkeep of the store, my primary responsibilites were helping people choose the right
            technology to fit their needs. Sold, set up, diagnosed and repaired everything from PCs and Macs to tablets and
            smartphones. My first real experience with consumer electronics.</div>
        </div>
      </li>

      <!-- Item 2 -->
      <li>
        <div class="direction-l">
          <div class="flag-wrapper">
            <span class="hexa"></span>
            <span class="flag">OfficeMax (Office Depot)</span>
            <span class="time-wrapper"><span class="time">OCT 2013</span></span>
          </div>
          <div class="desc">In addition to acting as manager-on-duty, coached others on sales and supervised the entire consumer electronics
            department. Responsible for meeting store goals in the sales, set-up and repair of computers, tablets, printers,
            etc.</div>
        </div>
      </li>

      <!-- Item 3 -->
      <li>
        <div class="direction-r">
          <div class="flag-wrapper">
            <span class="hexa"></span>
            <span class="flag">State Farm</span>
            <span class="time-wrapper"><span class="time">AUG 2015</span></span>
          </div>
          <div class="desc">While furthering my professional skills and obtaining a state insurance sales license, I often acted as the impromptu
            in-house technician. Whether finding better solutions to everyday tasks or helping coworkers with their computer
            troubles, I made it my mission to help keep the office running smoothly by sharing my love and knowledge of technology
            wherever and whenever I could.</div>
        </div>
      </li>

      <li>
        <div class="direction-l">
          <div class="flag-wrapper">
            <span class="hexa"></span>
            <span class="flag">Staples</span>
            <span class="time-wrapper"><span class="time">SEP 2016</span></span>
          </div>
          <div class="desc">For some extra income and an additional personal challenge, I picked up a second part time job at Staples. Here
            I kept the skills I had learned sharp by continuing to diagnose, repair, and sell personal computers and other
            consumer electronics. I acted as a trusted advisor for many customers seeking to make their next big decision
            on a computer or computer-related major purchase.</div>
        </div>
      </li>

      <li>
        <div class="direction-r">
          <div class="flag-wrapper">
            <span class="hexa"></span>
            <span class="flag">Citi</span>
            <span class="time-wrapper"><span class="time">FEB 2016</span></span>
          </div>
          <div class="desc">Here I shined as a team-player and contributor. While maintaining my own customer service metrics, I created and
            implemented software-based solutions to make day-to-day processes faster, easier, and more efficient. Also honed
            my skills in sales and brand representation.</div>
        </div>
      </li>

    </ul>


  </div>
</template>


<script>
  export default {
    name: 'resume',
    mounted() {
      window.sr = ScrollReveal({ duration: 2000 });
      sr.reveal('.main-title');
      sr.reveal('.main-subtitle');      
      sr.reveal('.flag-wrapper');
      sr.reveal('.flag');
      sr.reveal('.desc');
      sr.reveal('.direction-r');
      sr.reveal('.direction-l');
      sr.reveal('.hexa');
      sr.reveal('.time-wrapper');
      sr.reveal('.time');
    },
    data() {
      return {

      }
    }
  }

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  /* .main-title {
    margin-top: 3vh;
  } */

  .main-subtitle {
    color: white;
    text-align: center;
    font-family: 'Cinzel';
    letter-spacing: 3px;
    text-decoration: none !important;
    font-size: 1rem;
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

  .hexa {
    border: 0px;
    float: left;
    text-align: center;
    height: 35px;
    width: 60px;
    font-size: 22px;
    background: #f0f0f0;
    color: #3c3c3c;
    position: relative;
    margin-top: 15px;
  }

  .hexa:before {
    content: "";
    position: absolute;
    left: 0;
    width: 0;
    height: 0;
    border-bottom: 15px solid #f0f0f0;
    border-left: 30px solid transparent;
    border-right: 30px solid transparent;
    top: -15px;
  }

  .hexa:after {
    content: "";
    position: absolute;
    left: 0;
    width: 0;
    height: 0;
    border-left: 30px solid transparent;
    border-right: 30px solid transparent;
    border-top: 15px solid #f0f0f0;
    bottom: -15px;
  }

  .timeline {
    position: relative;
    padding: 0;
    width: 100%;
    margin-top: 20px;
    list-style-type: none;
  }

  .timeline:before {
    position: absolute;
    left: 50%;
    top: 0;
    content: ' ';
    display: block;
    width: 2px;
    height: 100%;
    margin-left: -1px;
    background: rgb(213, 213, 213);
    background: -moz-linear-gradient(top, rgba(213, 213, 213, 0) 0%, rgb(213, 213, 213) 8%, rgb(213, 213, 213) 92%, rgba(213, 213, 213, 0) 100%);
    background: -webkit-linear-gradient(top, rgba(213, 213, 213, 0) 0%, rgb(213, 213, 213) 8%, rgb(213, 213, 213) 92%, rgba(213, 213, 213, 0) 100%);
    background: -o-linear-gradient(top, rgba(213, 213, 213, 0) 0%, rgb(213, 213, 213) 8%, rgb(213, 213, 213) 92%, rgba(213, 213, 213, 0) 100%);
    background: -ms-linear-gradient(top, rgba(213, 213, 213, 0) 0%, rgb(213, 213, 213) 8%, rgb(213, 213, 213) 92%, rgba(213, 213, 213, 0) 100%);
    background: linear-gradient(to bottom, rgba(213, 213, 213, 0) 0%, rgb(213, 213, 213) 8%, rgb(213, 213, 213) 92%, rgba(213, 213, 213, 0) 100%);
    z-index: 0 !important;
  }

  .timeline li {
    padding: 2em 0;
  }

  .timeline .hexa {
    width: 16px;
    height: 10px;
    position: absolute;
    background: #19f6e8;
    z-index: 5;
    left: 0;
    right: 0;
    margin-left: auto;
    margin-right: auto;
    top: -30px;
    margin-top: 0;
  }

  .timeline .hexa:before {
    border-bottom: 4px solid #19f6e8;
    border-left-width: 8px;
    border-right-width: 8px;
    top: -4px;
  }

  .timeline .hexa:after {
    border-left-width: 8px;
    border-right-width: 8px;
    border-top: 4px solid #19f6e8;
    bottom: -4px;
  }

  .direction-l,
  .direction-r {
    float: none;
    width: 100%;
    text-align: center;
  }

  .flag-wrapper {
    text-align: center;
    position: relative;
  }

  .flag {
    font-family: 'Cinzel';
    position: relative;
    display: inline;
    background: black;
    z-index: 15;
    padding: 6px 10px;
    text-align: left;
    border-radius: 5px;
  }

  .direction-l .flag:after,
  .direction-r .flag:after {
    content: "";
    position: absolute;
    left: 50%;
    top: -15px;
    height: 0;
    width: 0;
    margin-left: -8px;
    border: solid transparent;
    border-bottom-color: rgb(255, 255, 255);
    border-width: 8px;
    pointer-events: none;
  }

  .direction-l .flag {
    -webkit-box-shadow: -1px 1px 1px rgba(0, 0, 0, 0.15), 0 0 1px rgba(0, 0, 0, 0.15);
    -moz-box-shadow: -1px 1px 1px rgba(0, 0, 0, 0.15), 0 0 1px rgba(0, 0, 0, 0.15);
    box-shadow: -1px 1px 1px rgba(0, 0, 0, 0.15), 0 0 1px rgba(0, 0, 0, 0.15);
  }

  .direction-r .flag {
    -webkit-box-shadow: 1px 1px 1px rgba(0, 0, 0, 0.15), 0 0 1px rgba(0, 0, 0, 0.15);
    -moz-box-shadow: 1px 1px 1px rgba(0, 0, 0, 0.15), 0 0 1px rgba(0, 0, 0, 0.15);
    box-shadow: 1px 1px 1px rgba(0, 0, 0, 0.15), 0 0 1px rgba(0, 0, 0, 0.15);
  }

  .time-wrapper {
    display: block;
    font-family: 'Raleway';
    position: relative;
    margin: 4px 0 0 0;
    z-index: 14;
    line-height: 1em;
    vertical-align: middle;
    color: #fff;
  }

  .direction-l .time-wrapper {
    float: none;
  }

  .direction-r .time-wrapper {
    float: none;
  }

  .time {
    background: #19f6e8;
    color: rgba(0, 0, 0, .8);
    display: inline-block;
    padding: 8px;
  }

  .desc {
    font-family: 'Raleway';
    position: relative;
    margin: 1em 0 0 0;
    padding: 1em;
    background: black;
    -webkit-box-shadow: 0 0 1px rgba(0, 0, 0, 0.20);
    -moz-box-shadow: 0 0 1px rgba(0, 0, 0, 0.20);
    box-shadow: 0 0 1px rgba(0, 0, 0, 0.20);
    z-index: 15;
  }

  .direction-l .desc,
  .direction-r .desc {
    position: relative;
    margin: 1em 1em 0 1em;
    padding: 1em;
    z-index: 15;
  }

  @media(min-width: 768px) {
    .timeline {
      width: 660px;
      margin: 0 auto;
      margin-top: 20px;
    }

    .timeline li:after {
      content: "";
      display: block;
      height: 0;
      clear: both;
      visibility: hidden;
    }

    .timeline .hexa {
      left: -28px;
      right: auto;
      top: 8px;
    }

    .timeline .direction-l .hexa {
      left: auto;
      right: -28px;
    }

    .direction-l {
      position: relative;
      width: 310px;
      float: left;
      text-align: right;
    }

    .direction-r {
      position: relative;
      width: 310px;
      float: right;
      text-align: left;
    }

    .flag-wrapper {
      display: inline-block;
    }

    .flag {
      background: rgba(0, 0, 0, .25);
      font-size: 18px;
    }

    .direction-l .flag:after {
      left: auto;
      right: -16px;
      top: 50%;
      margin-top: -8px;
      border: solid transparent;
      border-left-color: rgb(254, 254, 254);
      border-width: 8px;
    }

    .direction-r .flag:after {
      top: 50%;
      margin-top: -8px;
      border: solid transparent;
      border-right-color: rgb(254, 254, 254);
      border-width: 8px;
      left: -8px;
    }

    .time-wrapper {
      display: inline;
      vertical-align: middle;
      margin: 0;
    }

    .direction-l .time-wrapper {
      float: left;
    }

    .direction-r .time-wrapper {
      float: right;
    }

    .time {
      padding: 5px 10px;
    }
    .desc {
      background-color: rgba(0, 0, 0, .25);
    }

    .direction-r .desc {
      margin: 1em 0 0 0.75em;
    }
  }

  @media(min-width: 992px) {
    .timeline {
      width: 800px;
      margin: 0 auto;
      margin-top: 20px;
    }

    .direction-l {
      position: relative;
      width: 380px;
      float: left;
      text-align: right;
    }

    .direction-r {
      position: relative;
      width: 380px;
      float: right;
      text-align: left;
    }
  }
</style>