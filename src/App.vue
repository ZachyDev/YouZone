<template>
  <div class="container">
    <SearchBar @termChange="onTermChange"></SearchBar>
    <VideoList 
    :videos="videos"
    @videoSelect="onVideoSelect"
    />
  </div>
</template>

<script>
import axios from 'axios';
import SearchBar from './components/SearchBar';
import VideoList from './components/VideoList';
const API_KEY = 'AIzaSyDXsjl0WnbpJtOV2hmWV3hb3C1fn-woNto';
export default {
  name: 'App',
  data() {
    return {
      videos: []
    }
  },
  components: {
    SearchBar,
    VideoList
  },
  methods: {
    // onvideo select
    onVideoSelect(video) {
      console.log(video)
    },
    // input from the user
    onTermChange: function(searchItem) {
      axios.get('https://www.googleapis.com/youtube/v3/search',{
        params: {
          key: API_KEY,
          type: 'video',
          part: 'snippet',
          q: searchItem
        }
      })
      .then(response => {
        console.log(response)
       this.videos = response.data.items;
      })
    }
  }

};
</script>

