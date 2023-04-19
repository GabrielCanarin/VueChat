<template>
  <header>
    <img src="./assets/Karta_logo.svg" class="Logo" alt="Karta logo">
  </header>
  <main class="container">
    <SendArea />
  </main>
</template>

<script>
import SendArea from './components/SendArea.vue'

export default {
  name: 'App',
  components: {
    SendArea
  }
}
</script>

<style>
body {
  background: radial-gradient(50% 98.88% at 50% 50%, #292929 0%, #151515 71.87%, #151515 100%);
  font-family: 'Lato', sans-serif;
  font-family: 'Waiting for the Sunrise', cursive;
  display: flex;
}

#app {
  width: 100%;
}

.logo {
  position: absolute;
  left: 40px;
  top: 50px;
}

.container {
  margin: auto;
  width: 33%;
  display: flex;
  flex-direction: column;
}
</style>
