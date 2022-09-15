<template>
  <h1>Quote element, but where is the data?</h1>
  <p>{{ data }}</p>
</template>

<script setup>
  const props = defineProps({
    data: Object
  })

</script>