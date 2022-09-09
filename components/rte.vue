<template>
  <hr>
  <h1>RTE</h1>
  <div v-html="data.field_text">
  </div>
</template>

<script setup>
  const props = defineProps({
    data: Object
  })
</script>