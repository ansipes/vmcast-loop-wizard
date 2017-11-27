<template>
  <div id="app">
    <nav-bar @navigate="navigate"/>
    <div class="wizard-container">
      <div class="wizard">
        <stepper
          :steps="steps"
          :stepp="step"
        />
        <name-loop
          v-show="step == 0"
        />
        <select-videos
          v-show="step == 1"
        />
        <add-slide
          v-show="step == 2"
        />
        <custom-video
          v-show="step == 3"
        />
        <review
          v-show="step == 4"
        />
        <!-- <repeaters :repeaters="repeaters"/>
        <playlist :repeaters="repeaters"/> -->
      </div>
    </div>
  </div>
</template>

<script>
import NavBar from './components/NavBar'
import Stepper from './components/Stepper'
import NameLoop from './components/NameLoop'
import SelectVideos from './components/SelectVideos'
import AddSlide from './components/AddSlide'
import CustomVideo from './components/CustomVideo'
import Review from './components/Review'
import Repeaters from './components/Repeaters'
import Items from './components/Items'
import Playlist from './components/Playlist'

export default {
  name: 'app',
  components: {
    NavBar,
    Stepper,
    NameLoop,
    SelectVideos,
    AddSlide,
    CustomVideo,
    Review,
    Playlist,
    Repeaters,
    Items
  },
  data () {
    return {
      step: 0,
      steps: [
        {
          title: 'fa-pencil',
          symbol: '',
          color: '',
          route: '',
          index: 0
        },
        {
          title: 'fa-play-circle',
          symbol: '',
          color: '',
          route: '',
          index: 1
        },
        {
          title: 'fa-picture-o',
          symbol: '',
          color: '',
          route: '',
          index: 2
        },
        {
          title: 'fa-plus',
          symbol: '',
          color: '',
          route: '',
          index: 3
        },
        {
          title: 'fa-search',
          symbol: '',
          color: '',
          route: '',
          index: 4
        }
      ],
      repeaters: [
        {
          title: 'Advertisement',
          interval: 3,
          color: '#eb008b',
          type: 1
        },
        {
          title: 'Dynamic',
          interval: 5,
          color: '#7f3f97',
          type: 1
        }
      ]
    }
  },
  methods: {
    navigate (direction) {
      switch (direction) {
        case 0:
          if (this.step === 0) {
            break
          }
          this.step--
          break
        case 1:
          if (this.step === 4) {
            break
          }
          this.step++
          break
      }
    }
  }
}
</script>

<style>
  body {
    margin: 0;
  }
  * {
    font-family: "Open Sans";
    color: white;
  }
  html {
    background-color: black;
  }
  div {
    padding: 15px;
  }
  #app {
    padding: 0;
    margin: 0;
    width: 100%;
  }
  .wizard-container {
    padding: 0;
    margin: 0;
    display: flex;
    justify-content: center;
  }
  .wizard {
    width: 1080px;
    padding: 0;
    margin: 0;
  }
  @media only screen and (max-width: 900px) {
    .wizard {
      width: 100%;
    }
  }
  @media only screen and (max-width: 500px) {
    .wizard {
      width: 100%;
    }
  }
</style>
