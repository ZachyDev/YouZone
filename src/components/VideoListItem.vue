<template>
  <li>  {{ video.snippet.channelTitle }}</li>
</template>

<script>
export default {
    name: 'VideoListItem',
    props: ['video']
}
</script>

<style>

</style>