<template>
  <div>
    <h1>Make an Image or Text Slide</h1>
    <h4>Use a slide to promote your services, introduce your physicians, make an announement, and more.</h4>
    <div>
      <h3>Do You Want ViewMedica Videos in Your Loop?</h3>
      <button>Make a Slide</button>
      <button>No Thanks</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'add-slide',
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
