<template>
 <div>
  <ul v-bind:key="video.etag" v-for="video in videos">
     {{ video.snippet.channelTitle }}
    {{ video.snippet.description}}
  </ul>
 </div>
</template>

<script>
export default {
    name: 'VideoList',
    props: [ 'videos' ]
}
</script>

<style>

</style>