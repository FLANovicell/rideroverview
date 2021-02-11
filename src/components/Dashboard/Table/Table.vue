<template>
  <div class="table">
    <table>
      <tr>
        <th>Name</th>
        <th>Indoor</th>
        <th>Outdoor</th>
      </tr>
      <tr>
        <td>frans</td>
        <td><button @click="counter += 1"></button></td>
        <td>true</td>
      </tr>
    </table>
  </div>
</template>

<script>
export default {
  data() {
    return {
      counter: 0,
    };
  },
};
</script>

<style lang="scss" scoped>
table {
  width: 100%;
}
</style>
