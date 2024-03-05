<script>
import { createClient } from "@supabase/supabase-js";

export default {
  data() {
    return {
      firstName: "",
      lastName: "",
      email: "",
      website: "",
      message: "",
    };
  },
  methods: {
    async submitForm() {
      // Initialize Supabase client with your Supabase URL and API key
      const supabaseUrl = "https://axjbsqfusfjcefwpehcc.supabase.co";
      const supabaseKey =
        "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6ImF4amJzcWZ1c2ZqY2Vmd3BlaGNjIiwicm9sZSI6ImFub24iLCJpYXQiOjE3MDk2NTgyMDQsImV4cCI6MjAyNTIzNDIwNH0.qVkyJFKudOz3B4lhW4ntoH-d6tq-ZLduublCcuatuSk";
      const supabase = createClient(supabaseUrl, supabaseKey);

      // Send form data to Supabase
      try {
        const { data, error } = await supabase
          .from("contacts") // Replace 'contacts' with your Supabase table name
          .insert([
            {
              first_name: this.firstName,
              last_name: this.lastName,
              email: this.email,
              website: this.website,
              message: this.message,
            },
          ]);

        if (error) {
          console.error("Error inserting data:", error);
        } else {
          console.log("Data inserted successfully:", data);
          // Optionally, you can reset the form after successful submission
          this.resetForm();
        }
      } catch (error) {
        console.error("Error connecting to Supabase:", error);
      }
    },
    resetForm() {
      this.firstName = "";
      this.lastName = "";
      this.email = "";
      this.website = "";
      this.message = "";
    },
  },
};
</script>

<template>
  <div>
    <div class="contact-form">
      <form id="formData" @submit.prevent="submitForm">
        <p>Contact Us</p>
        <div>
          <input
            v-model="firstName"
            type="text"
            placeholder="First Name"
            required
          />
          <input
            v-model="lastName"
            type="text"
            placeholder="Last Name"
            required
          />
        </div>
        <div>
          <input v-model="email" type="text" placeholder="Email" required />
          <input
            v-model="website"
            type="text"
            placeholder="Website (optional)"
          />
        </div>
        <div>
          <textarea v-model="message" cols="30" rows="10" required></textarea>
        </div>
        <button type="submit" class="btn">Send</button>
      </form>
    </div>
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

input[type="text"],
[type="text"],
[type="text"],
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
