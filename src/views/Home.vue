<template>
  <div class="home">
    <h1 class="home-title">Dashboard</h1>
    <p class="home_intro">
      Choose your arena wether you are riding indoor or outdoor!
    </p>
    <Dashboard />
    <CreateUser />
  </div>
</template>

<script>
// @ is an alias to /src

import Dashboard from "@/components/Dashboard/Dashboard.vue";
import CreateUser from "@/components/Dashboard/CreateUser/CreateUser.vue";
export default {
  name: "Home",
  components: {
    Dashboard,
    CreateUser,
  },
};
</script>
<style lang="scss" scoped></style>
