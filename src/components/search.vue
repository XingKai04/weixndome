<template>
    <div class="search " :class="{focused:focused}" >
        <view class="search-box" > 
            <input @focus="gosearch" type="text" :placeholder="placeholder">
            <!-- <span v-show="span"></span> -->
        </view>
        <div class="" >
        <div href=""  :class="{dis:dis}" @click="qx" >取消</div>
        </div>
        <!-- 搜素遮罩层 -->
        <div class="result">

        </div>
    </div>
</template>

<script>
export default {
    data () {

     return{
         focused:false,
         placeholder:'',
         dis:'false'
        }
    },
    methods:{
        gosearch () {
            console.log('点击测试,输入框变色 ');
            this.focused=true;
            this.placeholder='输入你要的商品';
            this.dis=false;
        },
        qx () {
            console.log('111');
            this.focused=false;
            this.placeholder='';
            this.dis=true;
        }
    }
}
</script>

<style>
.dis {
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
    position: absolute;
    width: 100%;
    height:100% ;
    background-color: #ccc;
    z-index: 999;
}
.result {
    position: absolute;
    top: 100rpx;
    bottom: 0;
    left: 0;
    right: 0;
    background-color: #ffffff;
}


</style>
