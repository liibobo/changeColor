<template>
 <div class="app" ref="theme" theme='theme'>
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
    this.dom = this.$refs.theme;
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
.content {
  width: 100%;
  height: 100%;
  color: var(--fontColor);
  background: var(--bgColor);
}
</style>