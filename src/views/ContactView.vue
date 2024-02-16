<script setup>
import Alerts from "../components/Alerts.vue";
import Navbar from "../components/Navbar.vue";
import FooterModule from "../components/FooterModule.vue";
import Heading from "../components/Heading.vue";
</script>

<template>
  <div>
    <Alerts />
    <Navbar />
    <Heading />
    <div class="contact-form">
      <form id="formData">
        <p>Contact Us</p>
        <div>
          <input type="fname" placeholder="First Name" required />
          <input type="lname" placeholder="Last Name" required />
        </div>
        <div>
          <input type="email" placeholder="Email" required />
          <input type="website" placeholder="Website (optional)" />
        </div>
        <div>
          <textarea name="" id="" cols="30" rows="10" required></textarea>
        </div>
        <button class="btn">Send</button>
      </form>
    </div>
    <FooterModule />
  </div>
</template>

<style>
/* Apply styles to all textareas */
textarea {
  width: 900px;
  padding: 10px;
  margin-bottom: 10px;
  box-sizing: border-box; /* Ensure padding and border are included in the total width/height */

  /* Border and Box Shadow */
  border: 1px solid #ccc;
  border-radius: 4px;
  box-shadow: 0 0 5px rgba(0, 0, 0, 0.1);

  /* Font and Text Styles */
  font-family: "Arial", sans-serif;
  font-size: 14px;
  line-height: 1.4;
  color: #333;

  /* Resize behavior */
  resize: vertical; /* Allow vertical resizing */

  /* Transition for smooth effects (optional) */
  transition:
    border-color 0.3s,
    box-shadow 0.3s;
}

/* Change styles on focus */
textarea:focus {
  border-color: #007bff; /* Border color on focus */
  box-shadow: 0 0 8px rgba(0, 123, 255, 0.5); /* Box shadow on focus */
}

.contact-form {
  padding: 25px;
  text-align: center;
}

.contact-form p {
  font-weight: bold;
  font-family: sans-serif;
  font-size: 29px;
}

input[type="fname"],
[type="lname"],
[type="email"],
[type="website"] {
  width: 300px;
  padding: 12px 20px;
  margin: 5px;
  display: inline-block;
  height: 50px;
  border: 1px solid #ccc;
  border-radius: 3px;
  box-sizing: border-box;
}
.btn {
  /* background-color: white; */
  background-color: dodgerblue;
  color: white;
  border: none;
  padding: 10px;
  width: 125px;
  font-family: sans-serif;
  font-weight: bold;
  font-size: 20px;
  border-radius: 5px;
}

.btn:hover {
  cursor: pointer;
  background-color: blue;
}
</style>
