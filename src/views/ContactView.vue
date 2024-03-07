<script>
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
      "https://zfiuflvqtnvrjerianka.supabase.co",
      "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6InpmaXVmbHZxdG52cmplcmlhbmthIiwicm9sZSI6ImFub24iLCJpYXQiOjE3MDk2NzkwMDksImV4cCI6MjAyNTI1NTAwOX0.a_Ysc4W54bXlh-Fd86L0tzNRnPsq_pa_i9GJeazy74A",
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
  <form @submit.prevent="submitForm" id="contactForm">
    <div class="form-group">
      <label for="name">Name:</label>
      <input
        v-model="name"
        type="text"
        name="name"
        id="name"
        placeholder="Enter your name"
        required
      />
    </div>

    <div class="form-group">
      <label for="email">Email:</label>
      <input
        v-model="email"
        type="email"
        name="email"
        id="email"
        placeholder="Enter your email"
        required
      />
    </div>

    <div class="form-group">
      <label for="message">Message:</label>
      <textarea
        v-model="message"
        name="message"
        id="message"
        placeholder="Enter your message"
        required
      ></textarea>
    </div>

    <button type="submit">Submit</button>
  </form>
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
