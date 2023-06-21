<template>
  <div className="unsplash__tag container">
    <ul>
      <li>
        <a href="/"> apple </a>
      </li>
      <li>
        <a href="/"> banner </a>
      </li>
      <li>
        <a href="/"> tomato </a>
      </li>
      <li>
        <a href="/"> melon </a>
      </li>
      <li>
        <a href="/"> orange </a>
      </li>
    </ul>
  </div>
</template>
<style lang="scss" scoped>
.unsplash__tag {
  ul {
    display: flex;
    justify-content: center;
    margin-top: 100px;
    margin-bottom: 50px;
    li {
      a {
        border: 1px solid #e8ecf2;
        padding: 10px 20px;
        margin: 0 10px;
        color: #f7100d;
      }
    }
  }
}
</style>
