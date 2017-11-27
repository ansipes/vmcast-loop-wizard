<template>
  <div>
    <button @click="navigate(0)" class="back">Back</button>
    <button @click="navigate(1)" class="next">Next</button>
  </div>
</template>

<script>
export default {
  name: 'nav-bar',
  props: [
  ],
  data () {
    return {
    }
  },
  methods: {
    navigate (direction) {
      this.$emit('navigate', direction)
    }
  }
}
</script>

<style scoped>
  div {
    padding: 0;
    margin: 0;
    width: 100%;
    height: 50px;
    background-color: white;
    margin-bottom: 20px;
  }
  .back {
    background-color: #f6921c; /* Green */
    border: none;
    color: white;
    padding: 7px 20px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    width: 20%;
    border-radius: 0;
    height: 100%;
  }
  .next {
    background-color: #f6921c; /* Green */
    border: none;
    color: white;
    padding: 7px 20px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    width: 20%;
    border-radius: 0;
    height: 100%;
    float: right;
  }
</style>
