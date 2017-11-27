<template>
  <div>
    <h1>Welcome to the Loop Wizard</h1>
    <h4>This is a quick and easy way to make a broadcast Loop for your VMcast service. We'll walk you through the Loop-making process. When done, you can edit any of your Loop's features.</h4>
    <div class="item">
      <!-- <div class="step"><div class="circle"><p>1</p></div></div>
      <div class="info"><div class="circle"><i class="fa fa-question" aria-hidden="true"></i></div></div> -->
      <h3>Name Your Loop&nbsp;&nbsp;<i class="fa fa-pencil"></i></h3>
      <small>Loop Name&nbsp;&nbsp;<i class="fa fa-question-circle-o"></i></small>
      <br><br>
      <button>Save</button>
      <button>Cancel</button>
    </div>
    <div class="item">
      <h3>Select Your Loop Location in the VMcast Menu</h3>
      <button>Cancel</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'name-loop',
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
  .item {
    position: relative;
    background-color: #555;
    border-radius: 5px;
    margin-bottom: 10px;
  }
  .info {
    padding: 0;
    margin: 0;
    position: absolute;
    top: 0;
    right: 0;
    width: 35px;
    height: 35px;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .step {
    padding: 0;
    margin: 0;
    position: absolute;
    top: 0;
    left: 0;
    width: 35px;
    height: 35px;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .circle {
    padding: 0;
    margin: 0;
    width: 25px;
    height: 25px;
    background-color: gray;
    border-radius: 40px;
    display: flex;
    justify-content: center;
    align-items: center;
    transition: all 0.5s;
  }
</style>
