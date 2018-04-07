<template>
  <div class="logo">
      <div class="content w">
          <a href="#" class="toLogo">
              <img src="../assets/img/logo.png" alt="hecun-禾寸-进击的程序源 logo">
              <p class="slogo">Miracles sometimes occur, but one has to work terribly for them.</p>
          </a>
      </div>
  </div>
</template>
<script>
export default {};
</script>
<style lang="scss" scoped>
.content {
//   height: 80px;

  .toLogo {
    display: block;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    img {
      width: 180px;
    }

    .slogo {
      font-family: "Noto Sans";
      font-size: 12px;
      color: #aaa;
      text-align: center;
      margin-bottom: 5px;
    }
  }
}
</style>
