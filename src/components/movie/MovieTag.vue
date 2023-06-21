<template>
  <div className="movie__tag container">
    <ul>
      <li>
        <a href="/"> men </a>
      </li>
      <li>
        <a href="/"> girl </a>
      </li>
      <li>
        <a href="/"> tree </a>
      </li>
      <li>
        <a href="/"> apple </a>
      </li>
      <li>
        <a href="/"> water </a>
      </li>
    </ul>
  </div>
</template>
<style lang="scss" scoped>
.movie__tag {
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
