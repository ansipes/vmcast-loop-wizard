<template>
  <div class="slide-options">
    <slide-option/>
    <slide-option/>
    <slide-option/>
  </div>
</template>

<script>
import SlideOption from './SlideOption'
export default {
  name: 'slide-options',
  props: [
  ],
  components: {
    SlideOption
  },
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
.slide-options {
  width: 100%;
  display: -webkit-box;
  display: -moz-box;
  display: -ms-flexbox;
  isplay: -webkit-flex;
  display: flex;
  flex-flow:row;
  flex-wrap: nowrap;
  overflow-x: auto;
  -webkit-overflow-scrolling: touch;
  -ms-overflow-style: -ms-autohiding-scrollbar;
  margin: 0;
  padding: 0;
}
</style>
