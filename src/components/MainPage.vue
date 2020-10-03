<template>
  <div class="main">
    <main>
      <form @submit.prevent="getAvatar">
        <div class="img_container">
          <img :src="avatar" alt="avatar" class="avatar" />
        </div>
        <div class="formal_form">
          <label for="name">enter name</label>
        <input
          v-model="name"
          type="text"
          name="name"
          id="name"
          placeholder="enter name retard..."
        />
        <button type="submit">start!</button>
        </div>
      </form>
    </main>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "MainPage",
  data() {
    return {
      name: "",
      avatar: "https://api.adorable.io/avatars/170/abott@adorable.png"
    }
  },
  methods: {
    getAvatar() {
      this.avatar = `https://joeschmoe.io/api/v1/${this.name}`;
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
form {
  border: 3px solid #f1f1f1;
  padding: 0 10px;
}

input[type=text] {
  width: 100%;
  padding: 18px 6px;
  margin: 10px 0;
  display: inline-block;
  border: 1px solid #cccccc;
  box-sizing: border-box;
}

button {
  background-color: #ca0790;
  color: #f1f1f1;
  padding: 14px 20px;
  margin: 7px 0;
  border: none;
  cursor: pointer;
  width: 100%;
}

button:hover {
  opacity: 0.7;
}

.img_container {
  text-align: center;
  margin: 24px 0 12px 0;
}

img.avatar {
  width: 20%;
}

.formal_container {
  padding: 16px;
}
</style>
