<template>
  <section id="memberSection" :class="attr">
    <h3>멤버 소개</h3>
    <p>한국화가 맴버를 소개합니다.</p>
    <div class="member__inner container">
      <article class="member">
        <figure class="member__header">
          <img src="@/assets/images/icon/peep-1.svg" alt="멤버" />
        </figure>
        <div class="member__body">
          <h4>동양화작가</h4>
          <p class="desc">신윤복작가</p>
          <a href="/" class="btn"></a>
        </div>
      </article>
      <article class="member">
        <figure class="member__header">
          <img src="@/assets/images/icon/peep-2.svg" alt="멤버" />
        </figure>
        <div class="member__body">
          <h4>동양화작가</h4>
          <p class="desc">김홍도 작가</p>
          <a href="/" class="btn"></a>
        </div>
      </article>
      <article class="member">
        <figure class="member__header">
          <img src="@/assets/images/icon/peep-3.svg" alt="멤버" />
        </figure>
        <div class="member__body">
          <h4>동양화작가</h4>
          <p class="desc">김환기 작가</p>
          <a href="/" class="btn"></a>
        </div>
      </article>
    </div>
  </section>
</template>
<script>
export default {
  props: {
    attr: String,
  },
};
</script>
<style lang="scss">
//member__wrap
.member__inner {
  @include flex-between;

  .member {
    width: 32%;
    border: 2px solid var(--color_body);

    .member__header {
      margin-top: -20px;
      padding: 20px;

      img {
        width: 100%;
      }
    }
    .member__body {
      margin-top: -90px;
      padding: 15px 10px;
      background: #000;
      color: #fff;
      z-index: 100;
      position: relative;

      h4 {
        font-size: 22px;
      }

      a {
        color: #fff;
        text-decoration: underline;
        text-underline-position: under;
      }
    }
  }
}
</style>
