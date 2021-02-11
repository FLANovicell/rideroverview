<template>
  <div class="counter">
    <div class="counter__row">
      <div class="counter__indoor"></div>
    </div>
    <div class="counter__row">
      <div class="counter__outdoor"></div>
    </div>

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
export default {};
</script>

<style lang="scss" scoped>
.counter {
  &__row {
    display: inline-flex;
    width: 20%;
    height: 200px;
    background-color: red;
    margin: 10px;
  }
}
</style>
