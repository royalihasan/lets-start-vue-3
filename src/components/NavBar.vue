<template>
  <nav class="nav-container">
    <ul>
      <li>Home</li>
      <li>About</li>
      <li>Services</li>
      <li>Login</li>
    </ul>
    <div>
      <input type="text" name="search" id="search" />
    </div>
  </nav>
</template>

<style scoped>
.nav-container {
  display: flex;
  background-color: blueviolet;
  font-size: 1.2rem;
  height: 50px;
  align-items: center;
}
ul {
  list-style: none;
  color: white;
  display: flex;
}
li {
  margin-left: 23px;
  padding: 10px;
}
li:hover {
  border-bottom: 2px solid red;
}
input {
  border: none;
  outline: none;
  width: 330px;
  height: 25px;
  border-radius: 10px;
  margin-left: 20px;
}
</style>
