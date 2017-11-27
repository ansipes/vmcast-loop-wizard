<template>
  <div class="step">
    <div class="icon">
      <div class="circle" :style="{ 'background-color' : activeStep }">
        <p><i class="fa" aria-hidden="true"
            :class="step.title"
          ></i></p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'step',
  props: [
    'step',
    'stepp'
  ],
  data () {
    return {
    }
  },
  computed: {
    activeStep () {
      if (this.step.index <= this.stepp) {
        return '#f6921c'
      }
    }
  },
  methods: {
  }
}
</script>

<style scoped>
  p {
    padding: 0;
    margin: 0;
  }
  i {
    padding: 0;
    margin: 0;
  }
  .step {
    margin: 0;
    padding: 25px 0px;
    flex: 1;
    position: relative;
  }
  .circle {
    padding: 0;
    margin: 0;
    width: 35px;
    height: 35px;
    background-color: gray;
    border-radius: 40px;
    display: flex;
    justify-content: center;
    align-items: center;
    transition: all 0.5s;
  }
  .icon {
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 100%;
    position: absolute;
    top: 0;
    left: 0;
  }
  .progress {
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 100%;
    position: absolute;
    top: 0;
    left: 0;
  }
  .bar {
    padding: 0;
    background-color: #7f3f97;
    height: 5px;
    width: 100%;
  }
</style>
