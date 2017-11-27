<template>
  <div>
    <h1>Your Loop is Ready</h1>
    <h4>Launch your VMcast app and find this Loop in the "Loops" menu. Hit the "Review Your Loop" button below to see the complete Loop. There, you can rearrange the order of videos and edit its contents.</h4>
    <div>
      <h3>Do You Want to Review this Loop?</h3>
      <button>Review Loop</button>
      <button>Exit Wizard</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'review',
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
