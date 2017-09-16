<template>
  <div id="app">
    <div class="color-picker-container">
      <div class="color-column">
        <div class="colors-container" v-for="color in colors" :key="color.color">
          {{color.color}}
        </div>
      </div>
      <div class="color-variations"></div>
    </div>
  </div>
</template>

<script>
import colors from './colors.json';

export default {
  name: 'app',
  data() {
    return {
      colors: colors.materialColors,
    };
  },
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

  border-radius: 0.5rem;

  display: flex;
  flex-direction: row;
}

.color-column,
.color-variations {
  border: 1px solid black;
  height: 100%;
}

.color-column {
  flex: 1;
}

.color-variations {
  flex: 6;
}

</style>
