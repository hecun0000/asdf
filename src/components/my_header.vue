<template>
  <div class="my-header">
      <div class="header w">
         <nav class="nav">
           <div class="menu-box hidden-sm-and-up"  @click="toOpenMenu">
             <span class="menu" :class="openMenu?'toggle':''">

             </span>
           </div>
            <ul class="hidden-xs-only">
                <li v-for="(item,index) in navs" :key="index">
                    <a href="#" :alt="item.info+'禾寸-hecun-进击的程序员'">{{item.info}}</a>
                </li>
            </ul>
            <div class="connect">
                <i class="iconfont icon-qq2"></i>
                <i class="iconfont icon-github"></i>
                <i class="iconfont icon-weibo"></i>
                <i class="iconfont to-search"
                :class="toSearch?'icon-close':'icon-search'"
                 @click="toGoSearch"></i>
            </div>
        </nav>
      </div>
       <div class="search" :class="toSearch?'active': ''">
          <div class="w search-box">
            <label for="">搜索
              <input type="text" v-model="inputValue" autofocus @keydown.13="goSearch">
            </label>
          </div>
      </div>

      <div class="phone-nav hidden-sm-and-up" :class="openMenu?'active':''">
        <ul>
            <li v-for="(item,index) in navs" :key="index">
                <a href="#" :alt="item.info+'禾寸-hecun-进击的程序员'">{{item.info}}</a>
            </li>
        </ul>
      </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      toSearch: false,
      navs: [
        { info: "首页", to: "index" },
        { info: "分类", to: "index" },
        { info: "时间线", to: "index" },
        { info: "生活", to: "index" },
        { info: "关于我", to: "index" },
        { info: "联系我", to: "index" }
      ],
      inputValue: "",
      openMenu: false
    };
  },
  methods: {
    goSearch() {
      console.log("回车触发");
      if (this.inputValue) {
        // 暂时跳转至result页面
        this.$router.push("/result");
      }
    },
    toOpenMenu() {
      this.openMenu = !this.openMenu;
      this.toSearch = false;
    },
    toGoSearch() {
      this.toSearch = !this.toSearch;
      this.openMenu = false;
    }
  }
};
</script>
<style lang="scss" scoped>
.pop {
  position: absolute;
  top: 54px;
  left: 0;
  width: 100vw;
  height: calc(100vh - 54px);
  background: rgba(255, 255, 255, 0.8);
  transform: translateY(-3000px);
  transition: all 0.5s linear;
  z-index: 9;
  
  &.active {
    transform: translateY(0);
  }
}

// 小屏下的导航栏
.phone-nav {
  @extend .pop;
  ul li {
    text-align: center;
  }
}

// 搜索按钮
.menu-box {
  display: flex;
  align-items: center;
  cursor: pointer;
  .menu {
    display: block;
    width: 24px;
    height: 2px;
    background: #333;
    position: relative;
    &::before {
      position: absolute;
      content: "";
      width: 100%;
      background: inherit;
      height: 2px;
      top: -7px;
      transform-origin: 21.5px center;
      transform: rotateZ(0);
      transition: all 0.3s linear;
    }
    &::after {
      position: absolute;
      content: "";
      width: 100%;
      background: inherit;
      height: 2px;
      top: 7px;
      transform-origin: 21.5px center;
      transition: all 0.3s linear;
    }
    &.toggle {
      height: 0;
      &::after {
        transform: rotateZ(45deg);
      }
      &::before {
        transform: rotateZ(-45deg);
      }
    }
  }
}

.search {
  @extend .pop;

  .search-box {
    position: absolute;
    bottom: 100px;
    left: 0;
    right: 0;
    margin: auto;
    // width: 700px;
    text-align: center;

    input {
      display: block;
      width: 100%;
      border: none;
      outline: none;
      text-align: center;
      font-size: 60px;
      margin-top: 50px;
      border-bottom: 3px solid #999;
    }
  }
}

.my-header {
  height: 54px;
  line-height: 54px;
  border-bottom: 1px solid #ddd;
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  background: rgba(255, 255, 255, 0.9);
  padding: 0 20px;

  .header {
    position: absolute;
    left: 0;
    right: 0;
    top: 0;
    height: 100%;
    background: #fff;
    z-index: 10;
  }


  .nav {
    display: flex;
    justify-content: space-between;

    .connect {
      i {
        font-size: 18px;
        margin-right: 5px;
        color: #666;
        cursor: pointer;
      }
      .to-search {
        margin-left: 10px;
        font-size: 20px;
        color: #333;
        &:hover {
          color: #000;
          transform: scale(1.2);
        }
      }
      .icon-close {
        font-size: 16px;
      }
    }

    ul {
      display: flex;
      justify-content: flex-start;

      li {
        a {
          margin: 0 10px;
        }
      }
    }
  }
}
</style>
