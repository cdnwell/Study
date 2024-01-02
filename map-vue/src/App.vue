<script setup>
var map1;
window.onload = function(){
  map1 = new ngii_wmts.map("map1", {zoom : 2});
};
</script>

<template>
  <div id="map1" style="width:100%;height:100%;"></div>
</template>

<style scoped>
</style>
