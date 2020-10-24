<template>
  <router-link to="newcontact"
    ><h1>{{ msg }}</h1></router-link
  >
</template>

<script>
export default {
  name: "HelloWord",
  data() {
    return {
      msg: "Welcome",
    };
  },
};
</script>

<style>
h1 {
  font-weight: normal;
}
a {
  color: #42b983;
}
</style>