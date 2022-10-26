<template>
  <section id="imageType" class="image__wrap" :class="attr">
    <h2>우주🚀</h2>
    <p>우주는 더이상 갈 수 없는 영역이 아닙니다. 저희가 도와드리겠습니다.</p>
    <div class="image__inner" :class="layout">
      <article class="image img1">
        <h3 class="image__title">달 프로젝트</h3>
        <p class="image__desc">
          달에서 진행하는 사업에 대한 이야기를 나눠보도록 하겠습니다. 달은
          지금도 개발하고 있습니다 저희도 시대보다 앞서 가기위해서...
        </p>
        <a href="#">자세히보기</a>
      </article>
      <article class="image img2">
        <h3 class="image__title">은하 프로젝트</h3>
        <p class="image__desc">
          우리 은하계가 얼마나 많은 자원을 가지고 있는지 알고 있으십니까?
          은하계는 엄청난 가치를 지니고 있고 탐사를 위해 여러분에 도움이
          필요합니다.
        </p>
        <a href="#">자세히보기</a>
      </article>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    attr: String,
    layout: String,
  },
};
</script>

<style>
/* imageType */
.image__wrap > h2 {
  color: #fff;
}
.image__wrap > p {
  color: #a6b8c4;
}
.image__inner {
  display: flex;
  justify-content: space-between;
}

.image__inner .image {
  width: 48%;
  background: #ccc;
  color: #fff;
  box-sizing: border-box;
  padding: 180px 30px 30px 30px;
  border-radius: 20px;
}
.image__inner .img1 {
  background: url(../../assets/img/imageType01.jpg) no-repeat center / cover;
  margin-right: 20px;
}
.image__inner .img2 {
  background: url(../../assets/img/imageType02.jpg) no-repeat center / cover;
}

.image .image__title {
  font-size: 32px;
  line-height: 1.4;
  text-align: left;
}
.image .image__desc {
  font-size: 16px;
  line-height: 1.4;
  margin: 10px 0;
  text-align: left;
}
.image a {
  background-color: #b45a30;
  padding: 10px 20px;
  margin-top: 10px;
  display: inline-block;
  color: #fff;
}
@media (max-width: 960px) {
}
@media (max-width: 600px) {
  .image__inner {
    flex-direction: column;
  }
  .image__inner .image {
    width: 100%;
    padding: 205px 20px 20px 20px;
  }
  .image:first-child {
    margin-bottom: 20px;
  }
  .image__title {
    font-size: 24px;
  }
}
</style>
