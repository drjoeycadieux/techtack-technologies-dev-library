<script setup>
import Alerts from "../components/Alerts.vue";
import Navbar from "../components/Navbar.vue";
import FooterModule from "../components/FooterModule.vue";
</script>

<template>
  <div>
    <Alerts />
    <Navbar />
    <div class="about">
      <h1>About Us</h1>
      <p>Welcome to our website! Here's some information about us.</p>

      <h2>Our Api</h2>
      <p>
        Visit
        <a
          style="color: black; font-weight: bold"
          href="https://github.com/drjoeycadieux/techtack-technologies-api"
          >Visit Github for our api</a
        >
      </p>

      <h2>Team</h2>
      <ul>
        <li v-for="member in teamMembers" :key="member.id">
          {{ member.name }} - {{ member.role }}
        </li>
      </ul>
    </div>
    <FooterModule />
  </div>
</template>

<script>
export default {
  data() {
    return {
      teamMembers: [{ id: 1, name: "Joey Cadieux", role: "Developer" }],
    };
  },
};
</script>

<style>
.inner {
  padding: 1px;
  background-color: darkslateblue;
  width: 400px;
  margin: auto;
}
.about {
  max-width: 800px;
  margin: auto;
  padding: 20px;
}

h1,
h2 {
  color: #333;
  font-family: sans-serif;
}
p {
  font-family: sans-serif;
}

li {
  font-family: sans-serif;
  font-weight: bold;
}

ul {
  list-style-type: none;
  padding: 0;
}
</style>
