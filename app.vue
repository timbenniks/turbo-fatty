<template>
  <div>
    <h1>Data Sets</h1>
    <pre>{{ datasets }}</pre>

    <h1>Goals</h1>
    <pre>{{ goals }}</pre>
  </div>
</template>
<script lang="ts" setup>
const { data: datasets } = await useAsyncGql("datasets");
const { data: goals } = await useAsyncGql("goals");
</script>
