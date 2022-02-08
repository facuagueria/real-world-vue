<template>
  <p>Register for the event here.</p>
  <button @click="register">Register Me</button>
</template>

<script>
export default {
  name: "EventRegister",
  props: ["event"],
  methods: {
    register() {
      //Programmatic Navigation
      this.$router.push({
        name: "EventDetails",
      });
    },
  },
};
</script>

<style scoped></style>
