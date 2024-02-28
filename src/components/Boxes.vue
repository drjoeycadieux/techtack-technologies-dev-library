<script setup></script>

<template>
  <div>
    <div class="boxes-container">
      <div class="flex-boxes">
        <h1>Our Software Development</h1>
        <hr />
        <br />
        <div class="text">
          <img
            style="border-radius: 10px"
            class="img-responsive"
            src="../assets/dev-assets/host1.png"
            alt=""
            width="304"
            height="236"
          />
        </div>
        <div class="text">
          <img
            style="border-radius: 10px"
            class="img-responsive"
            src="../assets/dev-assets/host2.png"
            alt=""
            width="304"
            height="236"
          />
        </div>
        <div class="text">
          <img
            style="border-radius: 10px"
            class="img-responsive"
            src="../assets/host3.png"
            alt=""
            width="304"
            height="236"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<style>
.text {
  padding: 15px;
  color: white;
  font-family: sans-serif;
  width: 900px;
  margin: auto;
  display: inline;
}
.boxes-container {
  padding: 45px;
  /* background-color: #2d3748; */
  background-color: black;
  text-align: center;
}

.flex-boxes p {
  font-family: sans-serif;
  font-weight: bold;
  color: white;
  width: 900px;
  margin: auto;
  display: inline;
}

.flex-boxes h1 {
  color: white;
  padding: 5px;
  font-family: sans-serif;
}
</style>
