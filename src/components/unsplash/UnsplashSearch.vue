<template>
  <div className="unsplash__search container">
    <h2 className="blind">검색하기</h2>
    <input type="search" placeholder="검색해 주세요" />
    <button type="submit">검색하기</button>
  </div>
</template>
<style lang="scss">
@import "@/assets/scss/setting/mixins";
.unsplash__search {
  margin-bottom: 50px;
  text-align: center;
  input {
    border: 1px solid #e8ecf2;
    font-size: 16px;
    padding: 10px 20px;
    @include border(50px);
    min-width: 300px;
    margin-right: 10px;
    font-family: "aria";
  }
  button {
    @include button(#f7100d, #fff);
    @include border(50px);
  }
}
</style>
