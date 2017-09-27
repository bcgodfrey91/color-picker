<template>
  <div id="app">
    <div class="color-picker-container">
      <div class="color-column">
        <div
        class="color-container"
        v-for="color in colors"
        :key="color.colorName"
        v-bind="{ value: color.colorName }"
        v-bind:style="{ background: color.colorHex }"
        @click='fetchColor'>
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
  methods: {
    fetchColor(e) {
      console.log(e.target.getAttribute('value'));
    },
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
  height: 100%;
}

.color-column {
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  align-self: center;
  height: 95%;
}

.color-container {
  text-align: center;
  border-radius: 50%;
  width: 25px;
  height: 25px;
}

.color-variations {
  flex: 6;
}

</style>
