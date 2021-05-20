<template>
  <router-view/>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style lang="stylus">
body 
  overflow: hidden
html
  font-size: 16px; 
.icon
  width: 1em;
  height: 1em;
  vertical-align: -0.15em;
  fill: currentColor;
  overflow: hidden;
  font-size: 2rem
@media screen and (max-width:720px)
  html
    font-size: 10px;
</style>
