<template>
 <div class="app" theme='theme'>
    <div class="content">
      <p @click="changeTheme('theme')">白</p>
      <p @click="changeTheme('theme1')">换肤3</p>
      <p @click="changeTheme('theme2')">灰</p>
      <p @click="changeTheme('theme3')">换肤4</p>
    </div>
    <Home />
 </div>
</template>
<script>
import Home from './views/Home.vue';
export default {
  name: 'mine',
  data () {
  return {
    dom: null
  }
  },
  mounted() {
  },
  methods: {
  changeTheme (theme) {
    document.body.setAttribute('class', theme)
  }
  },
  components: {
    Home
  }
}
</script>
<style>
@import "./assets/scss/temp.css";
.app {
  width: 100%;
  height: 100vh;
  color: var(--fontColor);
  background: var(--bgColor);
}
</style>