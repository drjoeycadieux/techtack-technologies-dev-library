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
        &copy; Copytight 2020 - {{ currentYear }} Powered By TeamLitho. All
        Right Reserved. <a href="#">Terms of Services</a> |
        <a href="#">Privacy</a>
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
  font-size: 20px;
  font-family: sans-serif;
  text-align: center;
}

.footer p a {
  color: lightgray;
  font-family: sans-serif;
}

.footer p a:hover {
  color: white;
}
</style>
