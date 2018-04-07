<template>
  <div class="index">
    <my-header></my-header>
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

export default {
  components: {
   myHeader,myFooter,banner
  }
}
</script>
<style lang="scss" scoped>

</style>
