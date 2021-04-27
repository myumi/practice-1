<template>
  <div id="container">
    <div class="left-side">
      <ChoosePlan />
    </div>
    <div class="right-side">
      <SplashImage />
      <About />
      <Notifications />
    </div>
  </div>
</template>

<script>
import SplashImage from './components/SplashImage.vue'
import About from './components/About.vue'
import ChoosePlan from './components/ChoosePlan'
import Notifications from './components/Notifications.vue'

export default {
  name: 'App',
  components: {
    About,
    ChoosePlan,
    SplashImage,
    Notifications
  }
}
</script>

<style>
html, body {
  height: 100%;
  margin: 0;
  padding: 0;
}

* {
  box-sizing: border-box;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

  background-color: #e0e5ee;
  color: #2c3e50;
  height: 100%;
}

h1, h2, h3, h4, h5 {
  margin: 0;
}

h1 {
  font-size: 18px;
  font-weight: 700;
}

h2 {
  font-size: 16px;
  font-weight: 700;
}

h4 {
  color: #999fa7;
  font-size: 12px;
  font-weight: 500;
  line-height: 1.6;
  max-width: 300px;
}

input[type=text], input[type=email] {
  display: block;
  border: 1px solid #d9d9d9;
  border-radius: 8px;
  -moz-border-radius: 8px;
  -webkit-border-radius: 8px;
  padding: 15px 12px;
  margin: 8px 0;
}

#container {
  display: flex;
  flex-direction: row;
  justify-content: center;
}

.left-side, .right-side {
  display: flex;
  flex-direction: column;
  margin: 15px 20px 0;
}

.left-side {
  width: 420px;
}

.right-side {
  justify-content: space-between;
  width: 350px;
}
</style>
