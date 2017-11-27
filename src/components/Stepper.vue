<template>
  <div class="stepper">
    <div class="p-container">
      <div class="progress">
        <div class="bar" :style="{ width: progress }"></div>
      </div>
    </div>
    <div class="steps">
      <step
        v-for="step in steps"
        :key="step.index"
        :step="step"
        :stepp="stepp"
      />
    </div>
  </div>
</template>

<script>
import Step from './Step'

export default {
  name: 'stepper',
  props: [
    'steps',
    'stepp'
  ],
  components: {
    Step
  },
  data () {
    return {
    }
  },
  computed: {
    progress () {
      var interval = 100 / (this.steps.length - 1)
      return interval * this.stepp + '%'
    }
  },
  methods: {
  }
}
</script>

<style scoped>
  .stepper {
    padding: 0;
    margin-bottom: 10px;
    position: relative;
  }
  .steps {
    display: flex;
    justify-content: space-between;
    width: 100%;
    padding: 0;
    margin: 0;
  }
  .p-container {
    position: absolute;
    top: 23px;
    left: 0;
    padding: 0;
    margin: 0;
    width: 100%;
    display: flex;
    justify-content: center;
  }
  .progress {
    width: 80%;
    padding: 0;
    height: 4px;
    background-color: lightgray;
  }
  .bar {
    padding: 0;
    height: 4px;
    background-color: #f6921c;
    transition: width 0.5s;
  }
</style>
