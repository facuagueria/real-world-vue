<template>
  <p>Register for the event here.</p>
  <button @click="register">Register Me</button>
</template>

<script>
export default {
  name: "EventRegister",
  props: ["event"],
  inject: ["GStore"],
  methods: {
    register() {
      this.GStore.flashMessage = `You are successfully registered for ${this.event.title}`;
      setTimeout(() => {
        this.GStore.flashMessage = "";
      }, 3000);
      //Programmatic Navigation
      this.$router.push({
        name: "EventDetails",
      });
    },
  },
};
</script>

<style scoped></style>
