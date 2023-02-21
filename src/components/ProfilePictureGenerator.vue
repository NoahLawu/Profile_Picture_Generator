<template>
  <div class="container">
    <form @submit.prevent="showImage" class="form">
      <input
        v-model="value"
        class="first"
        type="text"
        placeholder="Ketik nama Anda..."
      />
      <button class="second" type="submit">Buat Profile Picture!</button>
      <img class="img" alt="" :src="imgUrl" />
    </form>
  </div>
</template>

<script>
export default {
  name: "ProfilePictureGenerator",
  data() {
    return {
      value: "",
      imgUrl: "",
    };
  },
  methods: {
    showImage() {
      return (this.imgUrl = "https://robohash.org/" + this.value);
    },
  },
};
</script>

<style scoped>
.container {
  width: 100vw;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}

.form {
  display: flex;
  flex-direction: column;
  align-items: center;
  row-gap: 20px;
}

.img {
  display: block;
  border-radius: 50%;
  border: 1px solid grey;
  background-color: white;
}
.first {
  width: 250px;
  height: 25px;
  border-radius: 5px;
  display: block;
}
.second {
  width: 150px;
  height: 40px;
  background-color: seagreen;
  color: white;
  font: 14px/3 sans-serif;
  border-radius: 5px;
  padding-bottom: 45px;
  cursor: pointer;
  display: block;
}

input,
input::placeholder {
  font: 17px/3 sans-serif;
}
input {
  padding: 0 10px;
}
</style>
