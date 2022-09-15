<template>
  <hr>
  <h1>Image</h1>
  
  <picture>
    <template v-for="el in data.field_image_media.field_media_image.sources" :key="el.srcset">
      <source :media="el.media" :srcset="`https://headless.drupal.dk${el.srcset}`">    
    </template>
    <img v-bind:src="'https://headless.drupal.dk' + data.field_image_media.field_media_image.img_element.uri">
  </picture>
</template>

<script setup>
  const props = defineProps({
    data: Object
  })

</script>