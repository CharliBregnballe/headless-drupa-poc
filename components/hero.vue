<template>
  <h1>Hero Element, but where is the data?</h1>
  <p>{{ data }}</p>
</template>

<script setup>
  const props = defineProps({
    data: Object
  })

</script>