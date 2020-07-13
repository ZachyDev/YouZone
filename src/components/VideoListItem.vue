<template>

  <li class="list-group-item media"> 
      <!-- thumbnail -->
       <img class="mr-3" :src="thumbnailUrl">
       <!-- video title -->
       <div class="media-body">
       {{ video.snippet.title }}
       </div>
 </li>
</template>

<script>
export default {
    name: 'VideoListItem',
    props: ['video'],
    computed: {
        thumbnailUrl() {
            return this.video.snippet.thumbnails.default.url;
        }
    }
}
</script>

<style>

</style>