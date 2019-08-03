<template>
    <div class="search">
        <view class="search-box" > 
            <input type="text">
            <span></span>
        </view>
        <!-- <a href="">取消</a> -->
    </div>
</template>

<script>
export default {
    data () {

        return{

        }
    }
}
</script>

<style>
.search {
    padding: 20rpx;
    background-color: #ea4451;
    
}
.search-box {
    height: 60rpx;
    padding: 0 30rpx 0 40rpx;
    background-color: aliceblue;
    border-radius: 8rpx;
    position: relative;
    
}
.search-box::after {
    content:'搜索';
    display: block;
    position: absolute;
    width: 96rpx;
    height: 50rpx;
    transform: translate(-50%,-50%);

    left: 50%;
    top: 50%;


}
input {
}
</style>
