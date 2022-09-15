<template>
  <div class="article_show">
    <h1>Article show page</h1>
    <!-- <picture>
      <template v-for="el in article.content.field_header.field_background.field_media_image.sources" :key="el.srcset">
        <source :media="el.media" :srcset="`https://headless.drupal.dk${el.srcset}`">    
      </template>
      <img v-bind:src="'https://headless.drupal.dk' + article.content.field_header.field_background.field_media_image.img_element.uri">
    </picture>
    
    <form :action="article.content.field_header.field_cta.url">
      <input type="submit" :value="article.content.field_header.field_cta.title" />
    </form>
    {{ 'https://headless.drupal.dk' + article.content.field_header.field_background.field_media_image.img_element.uri }} -->
    <p>{{ article.content.field_description }}</p>
  </div>
</template>

<script setup>
    const route = useRoute()
    
    const { data: article } = await useFetch(`https://headless.drupal.dk/news/${route.params.url}?format=json`)
</script>

<style lang="scss">
  .article_show {
    h1 {
      background: blue;
    }
  }
</style>