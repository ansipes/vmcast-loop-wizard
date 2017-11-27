<template>
  <div>
    <h1>Add a Custom Video</h1>
    <h4>You can add a YouTube video or a video from your own server. Custom videos are great ways to feature physicians, protocol, and other information.</h4>
    <div>
      <h3>Do You Want to Add a Custom Video to this Loop?</h3>
      <button>Add a Video</button>
      <button>No Thanks</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'custom-video',
  props: [
  ],
  data () {
    return {
    }
  }
}
</script>

<style scoped>
  div {
    text-align: center;
  }
  input {
    border-radius: 5px;
    border: none;
    padding: 10px 20px;
    color: black;
    font-size: 14px;
  }
  input:focus,
  select:focus,
  textarea:focus,
  button:focus {
    outline: none;
  }
  button {
    background-color: #f6921c; /* Green */
    border: none;
    color: white;
    padding: 7px 20px;
    margin: 0 0 10px 10px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    width: 150px;
  }
</style>
