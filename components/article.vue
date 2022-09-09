<template>
  <hr>
  <h1>Article</h1>
  <div v-for="article in data.field_articles.entities" :key="article.id">
    <img v-bind:src="'https://headless.drupal.dk' + article.field_list_media.field_media_image.sources[0].srcset" /> 
    <p>{{article.field_description}}</p>
  </div>
  
</template>

<script setup>
  const props = defineProps({
    data: Object
  })
</script>