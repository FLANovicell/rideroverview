<template>
  <div>
    <div class="counter">
      <div class="counter__row">
        <div class="counter__col">
          <div class="counter__indoor">Indoor {{ inCounter }}</div>
        </div>
        <div class="counter__col">
          <div class="counter__outdoor">Outdoor {{ outCounter }}</div>
        </div>
      </div>
    </div>
    <table class="table">
      <tr>
        <th>Name</th>
        <th class="table__indoor">Indoor</th>
        <th class="table__outdoor">Outdoor</th>
      </tr>
      <tr v-for="person in data.persons" :key="person.id">
        <td>{{ person.name }}</td>
        <td>
          <button
            :class="{ purple: inClicked }"
            class="table__button--indoor"
            @click="
              inCounter += 1;
              inClicked = !inClicked;
            "
          ></button>
        </td>
        <td>
          <button
            :class="{ green: outClicked }"
            class="table__button--outdoor"
            @click="
              outCounter += 1;
              outClicked = !outClicked;
            "
          ></button>
        </td>
      </tr>
    </table>
  </div>
</template>

<script>
import data from "/static/data.json";

export default {
  data() {
    return {
      inClicked: false,
      outClicked: false,
      data: data,
      inCounter: 0,
      outCounter: 0,
    };
  },
};
</script>

<style lang="scss" scoped>
.counter {
  &__row {
    display: inline-flex;
    width: 20%;
    height: 200px;
    margin: 10px;
    border-radius: 25%;
    justify-content: center;
    font-size: 2em;
    color: #fff;
  }
  &__col {
    margin: 5%;
  }
  &__indoor {
    background-color: purple;
    padding: 10px;
  }
  &__outdoor {
    background-color: green;
    padding: 10px;
  }
}

.table {
  width: 100%;
  &__indoor {
    background-color: purple;
    color: #fff;
  }
  &__outdoor {
    background-color: green;
    color: #fff;
  }
}
button {
  width: 100%;
  height: 50px;
}
table,
th {
  border: 2px solid rgb(51, 48, 48);
}
th {
  height: 50px;
}
.purple {
  background-color: purple;
}

.green {
  background-color: green;
}
</style>
