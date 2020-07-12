<template>
 <div>
  <ul v-bind:key="video.id" v-for="video in videos">
    {{ video.id}}
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