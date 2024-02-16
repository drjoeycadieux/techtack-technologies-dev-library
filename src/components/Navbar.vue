<script></script>

<template>
  <div class="navbar-menu">
    <ul>
      <p class="title">Techtack-Technoogies Dev Library</p>
      <router-link class="linknav" to="/">Home</router-link>
      <router-link class="linknav" to="/about">About</router-link>
    </ul>
  </div>
</template>

<style>
.navbar-menu {
  padding: 25px;
  background-color: #32394e;
}
.title {
  display: inline;
  margin: 8px;
  font-family: sans-serif;
  font-weight: bold;
  color: white;
  font-size: 26px;
}
.navbar-menu ul {
  display: block;
}
.linknav {
  color: white;
  text-decoration: none;
  font-family: sans-serif;
  margin: 8px;
}
.linknav:hover {
  color: lightgray;
  text-decoration: underline;
  font-weight: bold;
}
</style>
