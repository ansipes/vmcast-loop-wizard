<template>
  <div class="slide-option">
    <div class="slide-option-image-container">
      <img class="slide-option-image" src="https://animatedanatomy.com/images/16-9-dummy-image6.jpg"/>
    </div>
    <div class="slide-option-text">
      <h4>Type of Slide</h4>
      <p>This is a description of what this type of slide can do.</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'slide-option',
  props: [
  ],
  data () {
    return {
    }
  },
  computed: {
  },
  methods: {
  }
}
</script>
<style>
.slide-option {
  height: auto;
  flex: 1;
  background-color: white;
  border-radius: 5px;
  padding: 0px;
  overflow: hidden;
  margin: 0 10px;
}

.slide-option h4, p {
  color: black;
}
.slide-option-image-container {
  padding: 0;
  margin: 0;
  width: 100%;
}
.slide-option-image {
  padding: 0;
  margin: 0;
  width: 100%;
  height: auto;
}

@media only screen and (max-width: 500px) {


  .slide-option {
    min-width: 80%;
  }

  .slide-option:first-of-type {
    margin-left: 20px;
  }

  .slide-option:last-of-type {
  }
}
</style>
