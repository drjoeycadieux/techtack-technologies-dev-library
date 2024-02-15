<script>
export default {
  data() {
    return {
      currentYear: new Date().getFullYear(),
    };
  },
};
</script>

<template>
  <div>
    <div class="footer">
      <p>
        &copy; Copytight 2020 - {{ currentYear() }} TeamLitho Company. All Right
        Reserved
      </p>
    </div>
  </div>
</template>

<style>
.footer {
  padding: 15px;
  background-color: #2d3748;
}

.footer p {
  color: white;
  font-weight: bold;
  font-size: 20px;
  font-family: sans-serif;
  text-align: center;
}
</style>
