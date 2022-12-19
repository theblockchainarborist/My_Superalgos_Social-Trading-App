<template>
<div class="home-main-div">
  <div class="sliding-background">
  <div class="grid" :style="homepagebackground">
      <div id="platform-div" class="tile-btn" v-on:click="launchPlatform">
        <p id="platform">Launch Platform</p>
      </div>
      <div id="social-trading-div" class="tile-btn" v-on:click="startSocialTrading">
        <p id="social-trading-btn">Start Social Trading</p>
      </div>
      <div id="machine-learning-div" class="tile-btn" v-on:click="startBitcoinFactory">
        <p id="bitcoin-factory-btn">Bitcoin Factory</p>
      </div>
      <div id="docs-div" class="tile-btn" v-on:click="viewDocs" >
        <p id="docs-btn">View Docs</p>
      </div>
      <div id="map-div" class="tile-btn" v-on:click="viewMap" >
          <p id="map-btn">Open Map</p>
      </div>
      <div id="charting-space-btn-div" class="tile-btn" v-on:click="openChartingSpace">
        <p id="charting-space-btn">Charting Space</p>
      </div>
      <div id="governance-btn-div" class="tile-btn" v-on:click="openGovernance">
        <p id="governance-btn">Governance</p>
      </div>
      <div id="profile-btn-div" class="tile-btn" v-on:click="viewProfile">
        <p id="profile-btn">My Profile</p>
      </div>
  </div>
  </div>
  </div>
</template>

<script>

import dashboardIcon from "../assets/dashboard.png"
import homepagebackground from "../assets/homePageBackground.jpg"




  export default {
    name: 'Home',
  components: { },
    // Receive incoming data from parent app 
    props: ["incomingData"],
    data () {
      return {
        dataKey: '',
        dataObjects: [],
        dashboardIcon: dashboardIcon
      }
    },
    computed: {
    },
    methods: {
      launchPlatform() {
        alert("This feature is still under construction - Coming Soon!")
      },
      startSocialTrading() {
        this.$router.push('/social-trading')
      },
      startBitcoinFactory() {
        alert("This feature is still under construction - Coming Soon!")
      },
      viewProfile() {
        this.$router.push('/profile')
      },
      viewMap() {
        window.location.href = "https://superalgos.gogocarto.fr/";
      },
      viewDocs() {
        window.location.href = "https://superalgos.org/Docs/Foundations/Book/user-manual.shtml";
      },
      openChartingSpace() {
        alert("This feature is still under construction - Coming Soon!")
      },
      openGovernance() {
        alert("This feature is still under construction - Coming Soon!")
      }
    },  
  };
</script>

<style scoped>

/* Background */

  .home-main-div {
    overflow: hidden;
    color: white;
    align-content: top;
    border: solid 2px black;
    border-radius: 8px;
    margin-right: 1vw;
    margin-left: 1vw;
    margin-bottom: 1em;
    height: 100%;
    width:  95%;
    align-self: end;
    min-height: 300px;
    box-shadow: 0px 2px 10px 4px rgb(44, 44, 44);
    justify-self: center;
    object-fit: cover;
  }

  .sliding-background {
    display: flex;
    position: relative;
    background: url('../assets/homePageBackground.jpg') repeat-x 0 / 100% auto;
    top: 1%;
    left: 0%;
    width: 100%;
    height: 100%;
    animation: slide 80s linear infinite;
    transition: all .1s ease-out;
    object-fit: cover;
    size: zoom;
}

@keyframes slide {
    0%{background-position: 0, 0, 0, 0;}
	100%{background-position: 1692px, 0, 0;}
}


/* Setup the grid for buttons */
  .grid {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr;
    grid-template-areas: 
    'platform social-trading map docs'
    'placeholder1 placeholder2 placeholder3 placeholder4';
    justify-self: center;
    align-content: center;
    width: 100%;
    height: 100%;
  }

  
/* Setup the Buttons */
  .tile-btn {
    display: flex;
    border: solid 2px rgb(80, 180, 211);
    height: 20vw;
    width: 20vw;
    margin: 1vw;
    justify-content: center;
    align-items: center;
    background: rgba(24, 25, 26, 0.527);
    text-align: center;
    align-self: center;
    cursor: pointer;
    border-radius: 30px;
    justify-self: center;
    font-size: 2.8vw;
    font-weight: 550;
    max-width: 300px;
    max-height: 300px;
  }

/* Handle the button hover */
  .tile-btn:hover {
    color: white;
    background-color: rgba(51, 51, 51, 0.726);
    height: 20vw;
    width: 20vw;
    border: solid 6px rgb(80, 180, 211);
    }


    #social-trading-div {
      text-align: center;
    }





a {
  text-decoration: none
}

.nav-bar {
  position: fixed;
}


</style>

