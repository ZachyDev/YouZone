<template>
  <li>  {{ videosList.snippet.channelTitle }}</li>
</template>

<script>
export default {
    name: 'VideoListItem',
    props: ['videosList']
}
</script>

<style>

</style>