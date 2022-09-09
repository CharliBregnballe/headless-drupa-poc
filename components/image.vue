<template>
  <hr>
  <h1>Image</h1>
  <img v-bind:src="'https://headless.drupal.dk' + data.field_image_media.field_media_image.sources[0].srcset" /> 
</template>

<script setup>
  const props = defineProps({
    data: Object
  })

</script>