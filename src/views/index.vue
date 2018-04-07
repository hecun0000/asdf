<template>
  <div class="index">
    <my-header></my-header>
    <logo></logo>
    <banner></banner>
      <div class="mian w">
        这是首页
      </div>
    <my-footer></my-footer>
  </div>
</template>
<script>
import myHeader from "@/components/my_header";
import myFooter from "@/components/my_footer";
import banner from "@/components/banner";
import logo from "@/components/logo";

export default {
  components: {
   myHeader,myFooter,banner,logo
  }
}
</script>
<style lang="scss" scoped>

</style>
