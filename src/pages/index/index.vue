<template>
  <div @click="clickHandle">
    <swiper indicator-dots autoplay interval='3000 ' circular >
    <swiper-item >
      <a href="">
        <img src="/static/uploads/banner1.png" alt="">
      </a>
    </swiper-item>
    <swiper-item>
      <a href="">
        <img src="/static/uploads/banner2.png" alt="">
      </a>
    </swiper-item>
    <swiper-item>
      <a href="">
        <img src="/static/uploads/banner3.png" alt="">
      </a>
    </swiper-item>
    </swiper>
  </div>
</template>

<script>
export default {

}


</script>

<style scoped>
swiper {
  height: 340rpx;
}
swiper img{
  width: 750rpx;
  height: 340rpx;
}

</style>
