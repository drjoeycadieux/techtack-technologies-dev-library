<script setup>
import Navbar from "../components/Navbar.vue";
import Boxes from "../components/Boxes.vue";
import Alerts from "../components/Alerts.vue";
import FooterModule from "../components/FooterModule.vue";
</script>

<template>
  <div>
    <Alerts />
    <Navbar />
    <div>
      <div class="container">
        <div class="text-container">
          <p>Techtack-Technologies Dev Library</p>
        </div>
        <br />
        <hr />
      </div>
      <div class="flexbox-container">
        <div class="boxes1">
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Rerum
            exercitationem debitis aspernatur. Quos aut minima deserunt maxime
            vero laborum temporibus quia voluptatibus alias fugit repellat, sit
            veritatis eaque officia culpa.
          </p>
        </div>
      </div>
      <br />
      <br />
      <div class="flexbox-container2">
        <div class="boxes1">
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Rerum
            exercitationem debitis aspernatur. Quos aut minima deserunt maxime
            vero laborum temporibus quia voluptatibus alias fugit repellat, sit
            veritatis eaque officia culpa.
          </p>
        </div>
      </div>
      <br />
      <Boxes />
    </div>
    <FooterModule />
  </div>
</template>

<style>
hr {
  width: 900px;
  margin: auto;
}
.container {
  padding: 25px;
  padding-top: 125px;
}

.container p {
  text-align: center;
  font-family: sans-serif;
  font-weight: bold;
  color: #2d3748;
  font-size: 30px;
}

.flexbox-container {
  padding: 125px;
  text-align: center;
  background-color: #2d3748;
  width: 900px;
  margin: auto;
  border-radius: 25px;
  margin-right: 5px;
}

.boxes1 p {
  color: white;
  font-family: sans-serif;
  text-align: center;
  font-size: 25px;
}

.flexbox-container2 {
  padding: 125px;
  text-align: center;
  background-color: #2d3748;
  width: 900px;
  margin: auto;
  border-radius: 25px;
  margin-left: 5px;
}

.boxes1 p {
  color: white;
  font-family: sans-serif;
  text-align: center;
  font-size: 25px;
}
</style>
