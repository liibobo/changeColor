<template>
 <div class="app" ref="theme" theme='theme'>
  <div class="content">
    <p @click="changeTheme('theme')">白</p>
    <p @click="changeTheme('theme1')">灰</p>
    <p @click="changeTheme('theme2')">换肤3</p>
    <p @click="changeTheme('theme3')">换肤4</p>
  </div>
 </div>
</template>
<script>
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
  }
}
</script>
<style lang="scss">
@import "./assets/scss/temp1.scss";
body {
  @include background_color;
  @include fontColor;
  @include btn_border;
}
.app {
  display: inline-block;
  height: 100%;
  width: 100%;
  p {
    display: inline-block;
    padding: 10px 20px;
    border-width: 1px;
    border-radius: 10px;
    border-style: solid;
    margin: 20px;
    cursor: pointer;
  }
}
</style>