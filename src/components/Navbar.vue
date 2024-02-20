<script></script>

<template>
  <div class="navbar-menu">
    <ul>
      <p class="title">Techtack-Technoogies Developers</p>
      <router-link class="linknav" to="/">Home</router-link>
      <router-link class="linknav" to="/about">About</router-link>
      <router-link class="linknav" to="/contact">Contact</router-link>
    </ul>
  </div>
</template>

<style>
.navbar-menu {
  padding: 10px;
  /* background-color: #32394e; */
  box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
  background-color: white;
}
.title {
  display: inline;
  margin: 8px;
  font-family: sans-serif;
  font-weight: bold;
  color: black;
  font-size: 30px;
}
.navbar-menu ul {
  display: block;
}
.linknav {
  color: #32394e;
  text-decoration: none;
  font-family: sans-serif;
  font-weight: bold;
  margin: 8px;
}
.linknav:hover {
  background-color: lightgray;
  opacity: 1.5;
  padding: 1rem;
  border-radius: 5px;
}
</style>
