<template>
  <div :class="{ 'container': true, 'dark-mode': isDarkMode }" :style="{ 'background-color': backgroundColor, 'color': textColor }">
    <p>Selamat datang di aplikasi apa hayo</p>
    <input type="text" v-model="inputText" placeholder="Masukkan teks di sini">
    <p>robot mengetik: {{ inputText }}</p>
    <button @click="toggleDarkMode">Mode Gelap</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isDarkMode: false,
      inputText: '',
      backgroundColor: 'lightgray',
      textColor: 'black'
    };
  },
  methods: {
    toggleDarkMode() {
      this.isDarkMode = !this.isDarkMode;
      if (this.isDarkMode) {
        this.backgroundColor = 'black';
        this.textColor = 'white';
      } else {
        this.backgroundColor = 'lightgray';
        this.textColor = 'black';
      }
    }
  }
};
</script>

<style scoped>
.container {
  width: 100%;
  padding: 20px;
}

.dark-mode {
  background-color: black;
  color: white;
}
</style>

