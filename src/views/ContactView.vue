<script>
import Navbar from "../components/Navbar.vue";

import { createClient } from "@supabase/supabase-js";

export default {
  data() {
    return {
      supabase: null,
      name: "",
      email: "",
      message: "",
    };
  },
  created() {
    this.supabase = createClient(
      "https://fatwsfvfwsnpomvxpeoq.supabase.co",
      "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6ImZhdHdzZnZmd3NucG9tdnhwZW9xIiwicm9sZSI6ImFub24iLCJpYXQiOjE3MDk3NDkyODYsImV4cCI6MjAyNTMyNTI4Nn0.k1vzT6m-c2RRliZER_RH6i1JQLz1ufTFFia1sM1hRvg",
    );
  },
  methods: {
    async submitForm() {
      const submission = {
        name: this.name,
        email: this.email,
        message: this.message,
      };

      const { error } = await this.supabase
        .from("contacts")
        .insert([submission], { returning: "minimal" });

      if (error) {
        alert("There was an error, please try again.");
      } else {
        alert("Thanks for contacting us.");
        // Clear form inputs after successful submission
        this.name = "";
        this.email = "";
        this.message = "";
      }
    },
  },
};
</script>

<template>
  <div>
    <Navbar />
    <div>
      <form @submit.prevent="submitForm" id="contactForm">
        <h2>Contact Us</h2>
        <input v-model="name" type="text" name="name" placeholder="Name" />
        <input v-model="email" type="email" name="email" placeholder="Email" />
        <textarea
          v-model="message"
          name="message"
          placeholder="Message"
        ></textarea>
        <button type="submit">Submit</button>
      </form>
    </div>
  </div>
</template>

<style scoped>
#contactForm {
  max-width: 400px;
  margin: auto;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 8px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

.form-group {
  margin-bottom: 15px;
}

label {
  display: block;
  font-weight: bold;
  margin-bottom: 5px;
}

input,
textarea {
  width: 100%;
  padding: 8px;
  box-sizing: border-box;
  border: 1px solid #ccc;
  border-radius: 4px;
  margin-top: 5px;
}

button {
  background-color: #4caf50;
  color: white;
  padding: 10px 15px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}
</style>
