<template>
  <hr>
  <h1>Article</h1>
  <div class="articles">
    <div v-for="article in data.field_articles.entities" :key="article.id" class="article">
      <img v-bind:src="'https://headless.drupal.dk' + article.field_list_media.field_media_image.img_element.uri" /> 
      <p>{{article.field_description}}</p>
      <p>{{ article.url }}</p>
      <NuxtLink :to="`${article.url}`">
        Go to article
      </NuxtLink>
  </div>
  </div>
  
</template>

<script setup>
  const props = defineProps({
    data: Object
  })
</script>

<style lang="scss">
  .articles {
    display: flex;

    .article {
      margin: 2em;
    }
  }
</style>