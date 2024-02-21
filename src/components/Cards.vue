<template>
  <div class="card-container">
    <div class="card" v-for="(card, index) in cards" :key="index">
      <div class="card-header">{{ card.title }}</div>
      <div class="card-body">{{ card.content }}</div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cards: [
        {
          title: "Technologies",
          content:
            "Certainly! Technologies is a broad term that encompasses various tools methods, and systems developed to solve problems or accomplish specific tasks. Here are some key areas within technology",
        },
        {
          title: "Software",
          content:
            "Software: Encompasses applications, operating systems, and programming languages.",
        },
        {
          title: "Development",
          content:
            "In the realm of technology, development often refers to the process of creating and maintaining software applications. It includes activities such as coding, testing, debugging, and deploying software.",
        },
      ],
    };
  },
};
</script>

<style scoped>
.card-container {
  display: flex;
  justify-content: space-between;
}

.card {
  width: 30%;
  border: 2px solid #ddd;
  border-radius: 8px;
  padding: 16px;
  margin-bottom: 20px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  font-family: sans-serif;
  cursor: pointer;
}

.card:hover {
  background-color: lightblue;
}

.card-header {
  font-size: 1.2em;
  font-weight: bold;
  margin-bottom: 8px;
}

.card-body {
  color: #555;
}
</style>
