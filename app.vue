<template>
  <div>
    <h1>Front Page</h1>
    
    <div v-for="content in frontpage.content.layout_builder__layout[0].regions.content" :key="content.id">      
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

        <template #default>
          Default
        </template>
      </v-switch>
    </div>
  </div>
</template>

<script setup>
  import VSwitch from '@lmiller1990/v-switch'

  const { data: frontpage } = await useFetch('https://headless.drupal.dk/?format=json')
</script>

<styles lang="scss">

</styles>