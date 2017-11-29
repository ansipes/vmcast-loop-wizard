<template>
  <div class="add-custom-video">
    <div class="slide-container">
      <div class="slide-video-container">
        <div class="slide-video">
          <div class="text-area">
            <div class="title">Title</div>
            <div class="text"></div>
          </div>
        </div>
      </div>
    </div>
    <div class="slide-settings">
      <p>"At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque corrupti quos dolores et quas molestias excepturi sint occaecati cupiditate non provident, similique sunt in culpa qui officia deserunt mollitia animi, id est laborum et dolorum fuga. Et harum quidem rerum facilis est et expedita distinctio. Nam libero tempore, cum soluta nobis est eligendi optio cumque nihil impedit quo minus id quod maxime placeat facere possimus, omnis voluptas assumenda est, omnis dolor repellendus. Temporibus autem quibusdam et aut officiis debitis aut rerum necessitatibus saepe eveniet ut et voluptates repudiandae sint et molestiae non recusandae. Itaque earum rerum h</p>
<p>"At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque corrupti quos dolores et quas molestias excepturi sint occaecati cupiditate non provident, similique sunt in culpa qui officia deserunt mollitia animi, id est laborum et dolorum fuga. Et harum quidem rerum facilis est et expedita distinctio. Nam libero tempore, cum soluta nobis est eligendi optio cumque nihil impedit quo minus id quod maxime placeat facere possimus, omnis voluptas assumenda est, omnis dolor repellendus. Temporibus autem quibusdam et aut officiis debitis aut rerum necessitatibus saepe eveniet ut et voluptates repudiandae sint et molestiae non recusandae. Itaque earum rerum h</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'add-custom-video',
  props: [
  ],
  data () {
    return {
      isMounted: false
    }
  },
  mounted () {
    this.isMounted = true
  },
  computed: {
  },
  methods: {
  }
}
</script>
<style>

.text-area {
  width: 100%;
  height: 100%;
  padding: 0px;
  margin: 0px;
  position: relative;
}

.title {
  width: 80%;
  height: 15%;
  background-color: white;
  padding: 0px;
  margin: 0px;
  position: absolute;
  top: 10%;
  left: 10%;
  color: black;
  text-align: left;
  font: 1em;
}

.text {
  width: 80%;
  height: 50%;
  background-color: white;
  padding: 0px;
  margin: 0px;
  position: absolute;
  top: 40%;
  left: 10%;
}


.slide-video-container {
  width: 100%;
  /* whatever width you want */
  display: inline-block;
  position: relative;
  padding: 0px;
  margin: 0px;
}


.slide-video-container:after {
  padding-top: 56.25%;
  /* 16:9 ratio */
  display: block;
  content: '';
}

.slide-video {
  padding: 0px;
  margin: 0px;
  position: absolute;
  top: 0;
  bottom: 0;
  right: 0;
  left: 0;
  /* fill parent */
  background-color: deepskyblue;
  /* let's see it! */
  color: white;
}



.add-custom-video {
  display: flex;
  flex-direction: row;
  padding: 0px;
  margin: 0px;
}
.slide-container {
  background-color: white;
  width: 50%;
  padding: 0px;
  margin: 0px;
  display: flex;
  align-items: flex-start;
  justify-content: center;
}
.slide-settings {
  background-color: red;
  width: 50%;
  padding: 0px;
  margin: 0px;
}

@media only screen and (max-width: 500px) {
  .add-custom-video {
    flex-wrap: wrap;
  }
  .slide-container {
    width: 100%;
  }
  .slide-settings {
    width: 100%;
  }
}

</style>
