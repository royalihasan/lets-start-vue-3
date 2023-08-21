<template>
  <h1>Add into Your Favorite</h1>

  <div class="main-container">
    <div class="list-wrapper">
      <ul v-for="item in listItem">
        <li>{{ item }}</li>
      </ul>
    </div>

    <div class="input-wrapper">
      <label for="fav-text">Your Favorite Text</label>
      <input type="text" name="fav-text" id="fav-text" v-model="inputItem" />
      <button @click="addToList">Add into List</button>
      <button @click="clearList">clear the List</button>
    </div>
  </div>
</template>

<script>
export default {
  data: () => {
    return {
      listItem: [],
      inputItem: " ",
    };
  },
  methods: {
    addToList() {
      this.listItem.push(this.inputItem);
    },
    clearList() {
      this.listItem = [];
    },
  },
  state: {},
  computed: {},
};
</script>

<style scoped>
.main-container {
  width: 100vw;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

.input-wrapper {}

.list-wrapper {}
</style>
