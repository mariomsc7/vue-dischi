<template>
  <div class="disc">
      <img :src="info.poster" :alt="info.title">
      <h1>{{ info.title }}</h1>
      <h2>{{ info.author }}</h2>
      <h3>{{ info.year }}</h3>
      <h4>{{ info.genre }}</h4>
  </div>
</template>

<script>
export default {
    name: 'Artists',
    props: ['info'],
}
</script>

<style>

</style>