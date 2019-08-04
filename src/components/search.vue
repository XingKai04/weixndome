<template>
    <div class="search " :class="{focused:focused}" >
        <view class="search-box" > 
            <input @focus="gosearch" type="text" :placeholder="placeholder">
            <!-- <span v-show="span"></span> -->
        </view>
        <div class="">
        <div href="" class="cancle">取消</div>
        </div>
    </div>
</template>

<script>
export default {
    data () {

     return{
         focused:false,
         placeholder:'',
         span:true
        }
    },
    methods:{
        gosearch () {
            console.log('点击测试,输入框变色 ');
            this.focused=true;
            this.placeholder='输入你要的商品';
            this.span=false;
        }
    }
}
</script>

<style>
.span {
    display: none;
} 
.search {
    display: flex;
    padding: 20rpx;
    background-color: #ea4451;
}
.search-box {
   
    height: 60rpx;
    padding: 0 30rpx 0 40rpx;
    background-color: aliceblue;
    border-radius: 8rpx;
    position: relative;
    flex: 1;
    
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
.search.focused {
background-color: #ccc;
}
.cancle {

display: none;
width: 150rpx;
}

</style>
