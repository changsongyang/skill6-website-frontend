<template>
  <div class="info-main">
    <info-left></info-left>
    <info-center></info-center>
    <info-right></info-right>
  </div>
</template>

<script>
import $ from 'jquery'

import InfoLeft from './home/InfoLeft'
import InfoRight from './home/InfoRight'
import InfoCenter from './home/InfoCenter'

export default {
  name: 'HomePreview',
  components: {
    InfoLeft,
    InfoRight,
    InfoCenter
  },
  mounted: function () {
    // 轮播立体效果
    $('#carousel').carousel({
      curDisplay: 1,
      autoPlay: false,
      interval: 1500
    })
  }
}
</script>

<style>
.info-main {
  display: -webkit-box;
  display: -moz-box;
  display: -ms-flexbox;
  display: -webkit-flex;
  display: flex;
  flex-direction: row;
  background-color: #fff;
  padding-top: 40px;
  padding-bottom: 40px;
  padding-left: 40px;
  padding-right: 30px;
  width: 100%;
  -webkit-box-orient: horizontal;
  -webkit-box-direction: normal;
  -webkit-flex-direction: row;
}

.info-flow-side {
  position: relative;
  display: block;
  width: 15%;
  background-color: crimson;
}
</style>
