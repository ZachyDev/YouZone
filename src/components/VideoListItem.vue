<template>
  <li class="list-group-item"> 
       {{ video.snippet.title }}
       <img :src="video.snippet.thumbnails.default.url">
 </li>
</template>

<script>
export default {
    name: 'VideoListItem',
    props: ['video']
}
</script>

<style>

</style>