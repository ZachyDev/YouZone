<template>
 <div>
   Videos Count: {{ videos.length}}
  <ul>
     <VideoListItem v-bind:key="video.etag" v-bind:videosList="video" v-for="video in videos" />
     
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