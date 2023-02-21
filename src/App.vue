<template>
  <ProfilePictureGenerator />
</template>

<script>
import ProfilePictureGenerator from "./components/ProfilePictureGenerator.vue";

export default {
  name: "App",
  components: {
    ProfilePictureGenerator,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  background-color: #e0ffff;
}
html,
body {
  height: 100%;
  margin: 0;
  padding: 0;
  overflow-x: hidden;
}
</style>
