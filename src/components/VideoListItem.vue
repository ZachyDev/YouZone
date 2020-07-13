<template>
  <li class="list-group-item"> 
       {{ video.snippet.title }}
       <img :src="thumbnailUrl">
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