<template>
  <div id="app">
    <div class="color-picker-container">
      <div class="color-column"></div>
      <div class="color-results-column"></div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'app',
};
</script>

<style>
html, body {
  height: 100%;
  width: 100%;
  margin: 0;
}

body {
  background: #0667d0;
}

#app {
  height: 100%;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.color-picker-container {
  background: #F8F8FF;
  height: 45rem;
  width: 30rem;

  border: 1px solid black;
  border-radius: 0.5rem;
}

</style>
