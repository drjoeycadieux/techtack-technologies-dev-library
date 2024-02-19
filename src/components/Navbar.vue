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
  padding: 25px;
  /* background-color: #32394e; */
  background-color: white;
}
.title {
  display: inline;
  margin: 8px;
  font-family: sans-serif;
  font-weight: bold;
  color: black;
  font-size: 26px;
}
.navbar-menu ul {
  display: block;
}
.linknav {
  color: black;
  text-decoration: none;
  font-family: sans-serif;
  margin: 8px;
}
.linknav:hover {
  background-color: lightgray;
  opacity: 1.5;
  padding: 1rem;
  border-radius: 5px;
}
</style>
