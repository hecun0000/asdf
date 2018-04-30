<template>
  <div class="index">
    <my-header></my-header>
    <logo></logo>
    <banner></banner>
    <list></list>
    <my-footer></my-footer>
  </div>
</template>
<script>
import myHeader from "@/components/my_header";
import myFooter from "@/components/my_footer";
import banner from "@/components/banner";
import logo from "@/components/logo";
import list from "@/components/list";

export default {
  components: {
   myHeader,myFooter,banner,logo,list
  }
}
</script>
<style lang="scss" scoped>

</style>
