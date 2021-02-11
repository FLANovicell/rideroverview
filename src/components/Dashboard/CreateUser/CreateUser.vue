<template>
  <div class="create">
    <div class="create__row">
      <h3>Create an user</h3>
    </div>
    <div class="create__row">
      <input placeholder="Name" v-model="name" />
      <button @click="addUser(name)">Create</button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: "",
      user: [],
      nextUserId: "",
      newUserName: "",
    };
  },
  methods: {
    addUser(name) {
      console.log(name);
      this.persons.push({
        id: this.nextUserId++,
        name: this.newUserName,
      });
      this.newUserName = "";
    },
  },
};
</script>

<style lang="scss" scoped></style>
