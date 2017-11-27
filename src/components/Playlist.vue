<template>
  <div>
    <button
      @click="toggleRepeaters"
      v-text="buttonText[showRepeaters]"
    ></button>
    <button
      @click="shuffle"
    >Shuffle</button>
    <h2>Loop</h2>
    <ul>
      <li
        v-for="item in playlist"
        :key="item.index"
        :style="{ 'background-color': item.color }"
      ><i class="fa fa-lg fa-bars move" aria-hidden="true"></i><i class="fa fa-lg fa-play-circle move" aria-hidden="true"></i>{{ item.title }}<i class="fa fa-lg fa-times-circle cancel" aria-hidden="true"></i></li>
    </ul>
  </div>
</template>

<script>
import _ from 'lodash'

export default {
  name: 'playlist',
  props: [
    'repeaters'
  ],
  computed: {
    playlist () {
      var playlist = []
      for (var i = 0; i < this.items.length; i++) {
        if (this.showRepeaters === 0) {
          for (var repeater of this.repeaters) {
            var interval = repeater.interval
            if (i % interval === 0 && i >= interval) {
              repeater.index = i
              playlist.push(repeater)
            }
          }
        }
        this.items[i].index = i
        playlist.push(this.items[i])
      }
      return playlist
    }
  },
  data () {
    return {
      showRepeaters: 1,
      buttonText: [
        'Hide Repeaters',
        'Show Repeaters'
      ],
      items: [
        {
          title: 'Cancer',
          color: '#24B2ED',
          type: 0
        },
        {
          title: 'Cardiovascular',
          color: '#24B2ED',
          type: 0
        },
        {
          title: 'Chiropractic',
          color: '#24B2ED',
          type: 0
        },
        {
          title: 'Complementary Medicine',
          color: '#24B2ED',
          type: 0
        },
        {
          title: 'Cosmetic Surgery',
          color: '#24B2ED',
          type: 0
        },
        {
          title: 'Dermatology',
          color: '#24B2ED',
          type: 0
        },
        {
          title: 'Ear, Nose and Throat',
          color: '#24B2ED',
          type: 0
        },
        {
          title: 'Gastrointestinal',
          color: '#24B2ED',
          type: 0
        },
        {
          title: 'General Health Care',
          color: '#24B2ED',
          type: 0
        },
        {
          title: 'Mental Health',
          color: '#24B2ED',
          type: 0
        },
        {
          title: 'Neurological',
          color: '#24B2ED',
          type: 0
        },
        {
          title: 'Ob/Gyn',
          color: '#24B2ED',
          type: 0
        },
        {
          title: 'Ophthalmology',
          color: '#24B2ED',
          type: 0
        },
        {
          title: 'Orthopedics',
          color: '#24B2ED',
          type: 0
        },
        {
          title: 'Pain Management',
          color: '#24B2ED',
          type: 0
        },
        {
          title: 'Physiatry',
          color: '#24B2ED',
          type: 0
        },
        {
          title: 'Podiatry',
          color: '#24B2ED',
          type: 0
        }
      ]
    }
  },
  methods: {
    toggleRepeaters () {
      switch (this.showRepeaters) {
        case 0:
          this.showRepeaters = 1
          break
        case 1:
          this.showRepeaters = 0
          break
      }
    },
    shuffle () {
      this.items = _.shuffle(this.items)
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
  button {
    float: right;
    background-color: #f6921c; /* Green */
    border: none;
    color: white;
    padding: 7px 20px;
    margin: 0 0 0 10px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
  }
  ul {
    margin: 0;
    padding: 0;
  }
  h2 {
    margin-top: 0;
  }
  li {
    border-radius: 5px;
    background-color: gray;
    list-style-type: none;
    padding: 10px;
    margin-bottom: 10px;
  }
  .cancel {
    float: right;
    padding-top: 4px;
  }
  .move {
    float: left;
    padding-top: 4px;
    padding-right: 10px;
  }
</style>
