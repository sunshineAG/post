
<style lang="less" scoped>
    .source-remixer-main{
        height:2000px;
        .remixer-adImg{
            width:110%;
            height:420px;
            position: absolute;
            top: 0;
        }
    }
</style>

<template>

    <div class="source-remixer-main">
        <div class="test" style="margin-left:-10px;width:104%;border-radius: 100% 100% 100% 100% / 0% 0% 24% 24%;overflow:hidden;position:relative;height:200px;background:#fff;">
            <img src="https://oktools.net/ph/400x320" alt="" class="remixer-adImg" >
        </div>
        <van-sticky @scroll="getInfoData($event)">
            <div v-if='hideFlag'>
                我是隐藏的组件吖
            </div>
            <div>主播</div>
        </van-sticky>
    </div>

</template>

<script>
import {Sticky} from "vant"
export default {
    name:'sourceInfo',
    components:{
        [Sticky.name]:Sticky
    },
    data(){
        return{
            hideFlag:false
        }
    },
    methods:{
        getInfoData(e){
            this.hideFlag = e.isFixed
        }
    }
}
</script>