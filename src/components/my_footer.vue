<template>
  <div class="my-footer">
      <div class="footer w">
            <logo></logo>
            <div class="contact text-align">
                <i class="iconfont icon-qq2"></i>
                <i class="iconfont icon-github"></i>
                <i class="iconfont icon-weibo"></i>
            </div>
            <div class="copy text-align">
                © 2017-2018 hecun.tech 版权所有 ICP证：陕ICP备17019364号
            </div>
      </div>
  </div>
</template>
<script>
import logo from './logo'
export default {
  data(){
      return {

      }
  },
  components:{
      logo
  }

}
</script>
<style lang="scss" scoped>
.my-footer{
    border-top: 1px solid #ddd;

    .text-align{
        text-align: center;
    }
    .copy{
        font-size: 12px;
        color: #999;
    }


}
</style>
