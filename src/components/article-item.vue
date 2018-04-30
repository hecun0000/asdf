<template>
  <div class="article">
      <div class="title">你不知道的JavaScript</div>
      <div class="info">
        <div class="classify">
          JavaScript
        </div>
        <div class="tags">
          <div class="tag">js </div>
          <div class="tag">css</div>
          <div class="tag">html</div>
          <div class="tag">vue</div>
        </div>
      </div>
      <div class="time">
        2018-03-12
      </div>
      <img src="../assets/img/banner/2.png" alt="">
      <div class="describe">
        forEach() 方法对每一个元素执行一次提供的函数 map() 方法创建一个新数组, 其结果是该数组都执行一次函数, 原数组保持不变 filter() 方法使执行测试数组的每一个函数, 并放回通过元素的新数组 some() 方法测试该数组有元素通过了指定函数的测试, 如果有返回true, 否则 ...
        <span class="more">READ MORE → </span>
      </div>
  </div>
</template>
<script>
export default {};
</script>
<style lang="scss" scoped>
.article {
  padding: 15px;
}

.title {
  font-size: 0.8rem;
}

.info {
  display: flex;
  flex-flow: wrap;
  // 分类
  .classify {
    border: 2px solid #000;
    padding: 2px 5px;
    cursor: pointer;
    margin-right: 20px;
    margin-bottom: 5px;
    &:hover {
      background: #000;
      color: #fff;
    }
  }

  // 标签
  .tags {
    display: flex;

    .tag {
      border: 1px solid #989;
      padding: 2px 5px;
      margin-right: 5px;
      border-radius: 3px;
      margin-bottom: 5px;
      cursor: pointer;
    }
  }
}

//时间
.time {
  color: #999;
  margin-top: 5px;
}

// 查看更多

.more {
  // display: inline-block;
  border-bottom: 2px solid #eee;
  cursor: pointer;

  &:hover {
    border-bottom: 2px solid #000;
  }
}
// 描述文字
.describe {
  padding: 5px;
  text-indent: 24px;
}
</style>

