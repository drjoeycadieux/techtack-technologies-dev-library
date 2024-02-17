<script setup>
import Alerts from "../components/Alerts.vue";
import Navbar from "../components/Navbar.vue";
import FooterModule from "../components/FooterModule.vue";
</script>

<template>
  <div>
  <Alerts/>
    <Navbar />
    <div class="about-content">
      <h1>General</h1>
      <p>
        <div class="inner"></div>
        <h5>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Eum voluptas officiis, harum ducimus impedit cumque architecto recusandae animi adipisci ratione, in nobis laudantium incidunt vitae, magni quia pariatur! Fuga, obcaecati!
        </h5>
      </p>
    </div>
    <FooterModule />
  </div>
</template>

<style>
.inner {
  padding: 1px;
  background-color: darkslateblue;
  width: 400px;
  margin: auto;
}
.about-content {
  padding: 15px;
  padding-top: 125px;
  text-align: center;
}

.about-content p {
  font-weight: bold;
  font-family: sans-serif;
  font-size: 26px;
  color: #2d3748;
}

.about-content h1 {
  color: black;
  font-family: sans-serif;
  font-weight: bold;
}
</style>
