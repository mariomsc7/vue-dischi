<template>
  <div class="search">
    <label for="type">Filter by gender :</label>
    <select v-model="searchFilter" name="type" id="type">
      <option disabled value="">Select a gender</option>
      <option value=""></option>
    </select>
  </div>
</template>

<script>
export default {
    name : 'Search',
    data() {
      return {
        searchFilter: '',
      }
    }
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