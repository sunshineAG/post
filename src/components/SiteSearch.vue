
<style lang="less" scoped>
    
</style>

<template>

    <div class="site-search-main">
        
        <div >这里是站内搜索

            <div @click="test">
                <van-search v-model="value" placeholder="请输入搜索关键词" />
            </div>
        </div>
        
    </div>

</template>

<script>
import {Search } from "vant"
export default {
    name:'SiteSearch',
    components:{
        [Search.name]:Search
    },
    data(){
        return{
            value:''
        }
    },
    methods:{
        test(){
            this.$router.push('/FilterSearch')
        },
        httpRequest(){
            
            // this.$axios({
            //     method:'POST',
            //     url:"",
            //     data:{}
            // }).then(res=>{

            // }).catch(error=>{

            //}).finally(() => {
            //       
            //    })

        }
    }
}
</script>