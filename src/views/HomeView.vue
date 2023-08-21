<script setup>
import NavBar from "../components/NavBar.vue";
</script>

<template>
  <main>
    <NavBar brandName="Alpha Traders" />
    <h1>Home</h1>
    <span>{{ sayHello() }}</span>
    <p v-if="2 == 2">
      {{ odd }}
    </p>
    <p v-else-if="2 > 3">"v-else"</p>
    <h2>Users List</h2>
    <ul v-for="user in users">
      <li>{{ user.id }}</li>
      <ul>
        <li>{{ user }}</li>
      </ul>
    </ul>
    <hr />
    <div class="counter">
      <label for="inc">How much Increment: </label>
      <input type="number" name="ic" id="inc" v-model.number="incrementBy" />
      <p>
        {{ count }}
        <!-- </p>   v-bind:value="incrementBy"
        v-on:input="incrementByInputValue" -->
      </p>
      <button v-on:click="increment">Increment</button>
    </div>
  </main>
</template>

<script>
export default {
  data: () => {
    return {
      incrementBy: 1,
      count: 0,
      odd: "This is Odd",

      users: [
        {
          id: "101",
          name: "Roy Ali Hasan",
          age: 21,
        },
      ],
    };
  },
  methods: {
    sayHello() {
      return "Hello from sayHello()";
    },
    increment() {
      this.count += this.incrementBy;
    },
    // incrementByInputValue(e) {
    //   this.incrementBy = Number(e.target.value);
    // },
  },
};
</script>

<style scoped>
.counter {
  margin-top: 50px;
  margin-left: 30px;
}
</style>
