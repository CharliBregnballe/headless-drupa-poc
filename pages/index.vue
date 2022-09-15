<template>
  <div>
    <h1>Front Page</h1>
    <div v-for="section in frontpage.content.layout_builder__layout" :key="section.id"> 
      <div v-for="content in section.regions.content" :key="content.id">   
        <v-switch :case="content.bundle">
        <template #rte>
          <Rte :data="content" />
        </template>

        <template #image>
          <Image :data="content" />
        </template>

        <template #articles>
          <Article :data="content" />
        </template>

        <template #article_form>
          <ArticleForm :data="content" />
        </template>

        <template #hero>
          <Hero :data="content" />
        </template>

        <template #quote>
          <Quote :data="content" />
        </template>

        <template #default>
          <h2>Unknown Element</h2>
        </template>
      </v-switch>
      </div>
    </div>
  </div>
</template>

<script setup>
  import VSwitch from '@lmiller1990/v-switch'

  const { data: frontpage } = await useFetch('https://headless.drupal.dk/?format=json')
</script>

<styles lang="scss">

</styles>