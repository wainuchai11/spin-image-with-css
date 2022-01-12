<template>
  <div class="card">
    <span style="--i:0;"></span>
    <img src="./assets/images/iPhone0.jpg" alt />
    <span style="--i:1;"></span>
    <img src="./assets/images/iPhone1.jpg" alt />
    <span style="--i:2;"></span>
    <img src="./assets/images/iPhone2.jpg" alt />
    <span style="--i:3;"></span>
    <img src="./assets/images/iPhone3.jpg" alt />
    <span style="--i:4;"></span>
    <img src="./assets/images/iPhone4.jpg" alt />
    <span style="--i:5;"></span>
    <img src="./assets/images/iPhone5.jpg" alt />
  </div>
</template>

<script>


export default {
  name: 'App',
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  background: #111;
}

.card {
  position: relative;
  width: 300px;
  height: 450px;
  display: flex;
  flex-direction: column;
}

.card span {
  position: absolute;
  top: 0;
  left: calc(100% / 6 * var(--i));
  width: calc(100% / 6);
  height: 100%;
}

.card img {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  opacity: 0;
  pointer-events: none;
}

.card img:nth-child(2),
.card span:hover + img {
  opacity: 1;
}
</style>
