<template>
 <div>
   Videos Count: {{ videos.length}}
  <ul v-bind:key="video.etag" v-for="video in videos">
     <VideoListItem></VideoListItem>
  </ul>
 </div>
</template>

<script>
import VideoListItem from './VideoListItem';
export default {
    name: 'VideoList',
    components: {
      VideoListItem
    },
    props: {
      videos: Array
    }
}
</script>

<style>

</style>