<template>
  <div>
    <ul>
      <li
        v-for="item in items"
        :key="item.title"
        v-text="item.title"
      ></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'items',
  props: [
    'items'
  ],
  data () {
    return {
    }
  }
}
</script>

<style>
</style>
