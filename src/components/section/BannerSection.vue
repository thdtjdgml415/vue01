<template>
  <section id="bannerType" class="banner__wrap" :class="attr">
    <h2 class="blind">배너 영역</h2>
    <div class="banner__inner">
      <h3 class="title">{{ banner[0].title }}</h3>
      <p class="desc">
        {{ banner[0].desc }}
        <a href="/" title="페이지 이동"> {{ banner[0].desc2 }}</a>
      </p>
      <span class="small blind">배너유형01</span>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    attr: String,
  },
  banner: [
    {
      title: "우주",
      desc: "미지의 탐사를 원하시는 분은",
      desc2: "많은 질문 부탁드리고 이곳을 클릭해주세요.",
    },
  ],
};
</script>

<style>
.banner__inner {
  background-image: url(../../assets/img/effect_bg_19@2x.jpg);
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  text-align: center;
  padding: 120px 0;
  color: #fff;
}
.banner__inner .title {
  font-size: 50px;
  line-height: 1.5;
  font-weight: 300;
  margin-bottom: 70px;
}
.banner__inner .desc {
  font-size: 24px;
  line-height: 1.5;
  font-weight: 300;
  margin-bottom: 70px;
}
.banner__inner .desc a {
  color: #fff;
  display: block;
}
.banner__inner .small {
  text-decoration: underline;
  font-size: underline;
}
@media (max-width: 960px) {
}
@media (max-width: 600px) {
  .banner__inner {
    padding: 80px 0;
  }
  .banner__inner .title {
    font-size: 30px;
    margin-bottom: 20px;
  }
  .banner__inner .desc {
    font-size: 16px;
    margin-bottom: 40px;
  }
}
</style>
