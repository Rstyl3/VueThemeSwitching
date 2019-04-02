<template>
  <div id="app" :class="changeTheme(themeColor)">
    <div class="btn-wrapper">
      <button @click="hdlDefault">Default Theme</button>
      <button @click="hdlDark">Dark Theme</button>
      <button @click="lightTheme">Light Theme</button>
    </div>
    <Header/>
    <Main/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'

export default {
  name: 'app',
  components: {
    Header,
    Main
  },
  data() {
    return {
      themeColor: ''
    }
  },
  methods: {
    changeTheme(c) {
      if (c == 'lightTheme') {
        return 'lightTheme'
      } else if (c == 'darkTheme') {
        return 'darkTheme'
      } else {
        return ':root'
      }
    },
    hdlDefault() {
      this.themeColor = ':root'
    },
    hdlDark() {
      this.themeColor = 'darkTheme'
    },
    lightTheme() {
      this.themeColor = 'lightTheme'
    }
  }
}
</script>

<style>
:root {
  --primary: darkorchid;
  --global-background: #ffeead;
  --secondary-background: #ffcc5c;
}
.darkTheme {
  --primary: white;
  --global-background: #000;
  --secondary-background: grey;
}
.lightTheme {
  --primary: #000;
  --global-background: white;
  --secondary-background: rgb(236, 235, 235);
}
.featured {
  --secondary-background: #ffe55b;
  --primary: #ff5564;
}

html,
body,
#app {
  margin: 0;
  padding: 0;
  height: 100%;
  width: 100%;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background: var(--global-background);
  color: var(--primary);
  padding-top: 50px;
}
.grid {
  display: grid;
  grid-template-columns: 200px 200px;
  grid-auto-rows: 140px;
  grid-gap: 20px;
  justify-content: center;
}
h1,
p {
  color: var(--primary);
  font-size: 18px;
  text-align: center;
}
a {
  text-decoration: none;
}
button {
  margin: 0px auto;
  display: block;
  padding: 5px 10px;
  border: none;
}
.btn-wrapper {
  display: flex;
}
</style>
