<template>
    <div class="list w">
        <div class="left">
            <article-item 
                v-for="(item,index) in 5" :key='index'
                :class="index!=0?'width-half':'' "
            ></article-item>
           <page-ctrl></page-ctrl> 
        </div>      
        <div class="right hidden-xs-only">
            <hot-article></hot-article>
        </div>
    </div>  
</template>
<script>
import articleItem from "./article-item";
import pageCtrl from "./pageCtrl";
import hotArticle from "./hot-article";
export default {
  components: {
    articleItem,
    pageCtrl,
    hotArticle
  }
};
</script>

<style lang="scss" scoped>
.list {
  display: flex;
  justify-content: space-between;

  .left {
    width: 900px;
    // border: 1px solid red;
    display: flex;
    flex-flow: wrap;
    justify-content: space-between;
  }

  .right {
    width: 300px;
    padding: 15px;
  }
}

@media only screen and (min-width: 641px) {
  .width-half {
    width: 48%;
  }
}
</style>
