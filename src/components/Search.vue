<template>
  <div class="search">
    <label for="type">Filter by genre s:</label>
    <select v-model="searchFilter" name="type" id="type">
      <option disabled value="">Select a genre</option>
      <option v-for="option in filter" :key="option.id">{{ option.genre }}</option>
    </select>
  </div>
</template>

<script>
export default {
    name : 'Search',
    props : ['filter']
}
</script>

<style scoped lang="scss">

  .search {
    text-align: center
  }

  .search {
    label {
      margin-right: 20px;
    }
  }

</style>