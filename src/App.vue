<template>
 <div class="app" ref="theme" theme='theme'>
   <Home />
  <div id="content">
    <p @click="changeTheme('theme1')">theme1</p>
    <p @click="changeTheme('theme2')">theme2</p>
    <p @click="changeTheme('theme3')">theme3</p>
  </div>
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
    this.dom.setAttribute('theme', theme)
  }
  },
  components: {
    Home
  }
}
</script>
<style lang="scss">
@import "./assets/scss/temp.scss";
body {
  @include background_color;
}
.app {
  display: inline-block;
  height: 100%;
  width: 100%;
  p {
    display: inline-block;
    &:first-child{
      background-color:red;
    }
    &:nth-child(2){
      background-color:#652BF5;
    }
    &:last-child{
      background-color:deepskyblue;
    }
  }
}
</style>