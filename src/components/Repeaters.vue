<template>
  <div>
    <h2>Repeaters</h2>
    <ul>
      <li
        v-for="repeater in repeaters"
        :key="repeater.title"
        :style="{ 'background-color': repeater.color }"
      >{{ repeater.title }} every {{ repeater.interval }} items</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'repeaters',
  props: [
    'repeaters'
  ],
  data () {
    return {
    }
  }
}
</script>

<style scoped>
  div {
    background-color: #555;
    border-radius: 5px;
    margin-bottom: 10px;
  }
  h2 {
    margin-top: 0;
  }
  ul {
    margin: 0;
    padding: 0;
  }
  li {
    border-radius: 5px;
    background-color: gray;
    list-style-type: none;
    padding: 10px;
    margin-bottom: 10px;
  }
</style>
