<template>
  <div>
    <SearchBar @termChange="onTermChange"></SearchBar>
    <VideoList v-bind:videos="videos"/>
    {{ videos.length }}
  </div>
</template>

<script>
import axios from 'axios';
import SearchBar from './components/SearchBar';
import VideoList from './components/VideoList';
const API_KEY = 'AIzaSyB5GqrHRaFYAJf1yUcipmZIWMRc8Rci5wE';
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
       this.videos = response.data.items;
      })
    }
  }

};
</script>

