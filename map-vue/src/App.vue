<script setup>
var map1;
window.onload = function(){
  map1 = new ngii_wmts.map("map1", {zoom : 2});
};



</script>

<template>
  <div class="map_frame">
    <div id="map1" style="width:100%;height:100%;">
      <div class="normal_map_div">
        <img class="normal_map" src="./assets/img/일반지도.png"/>
        <p>일반지도</p>
      </div>
      <div class="imagery_map_div">
        <img class="imagery_map" src="./assets/img/영상지도.png"/>
        <p>영상지도</p>
      </div>
    </div>
  </div>
</template>

<style scoped>
.map_frame {
  width: 100%;
  height: 100%;

  padding: 20px;
}

#map1 {
  position: relative;

  border-radius: 10px;

  overflow: hidden;
}

.normal_map_div
, .imagery_map_div {
  position: absolute;

  display: flex;
  flex-direction: column;

  width: 70px;
  height: 62px;

  border: 2px solid black;
  border-radius: 10px;

  z-index: 10;

  overflow: hidden;

  background-color: white;

  cursor: pointer;
}

.normal_map_div p
, .imagery_map_div p {
  display: flex;
  justify-content: center;

  font-size: 12px;
  font-weight: bold;

  border-top: 1px solid gray;
}

.normal_map_div {
  top: 30px;
  left: 30px;
}

.normal_map
, .imagery_map {
  width: 70px;
  height: 40px;
}

.imagery_map_div {
  top: 30px;
  left: 110px;
}
</style>
