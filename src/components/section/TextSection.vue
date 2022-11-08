<template>
  <section id="textType" class="text__wrap" :class="attr">
    <span class="blind">텍스트 유형01</span>
    <h2>{{ Texttitle[0].textTitle }}</h2>
    <div class="text__inner" :class="layout">
      <div
        class="text"
        :class="TextType.class"
        v-for="TextType in TextType"
        :key="TextType"
      >
        <h3 class="text__title">{{ TextType.title }}</h3>
        <p class="text__desc">
          {{ TextType.desc }}
        </p>
        <a class="text_btn" href="/">{{ TextType.detail }}</a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    attr: String,
    layout: String,
  },
  data() {
    return {
      TextType: [
        {
          class: "t1",
          title: "space",
          desc: "작년에 다양한 컨텐츠를 만들었던 Space 기업입니다.",
          detail: "더보기",
        },
        {
          class: "t2",
          title: "Tesla",
          desc: "전기차로 세계에서 손꼽히는 기업으로 거대규모의 기업입니다.",
          detail: "더보기",
        },
        {
          class: "t3",
          title: "MS",
          desc: "마이크로소프트는 소프트웨어에서 독보적인 기업입니다.",
          detail: "더보기",
        },
        {
          class: "t4",
          title: "Samsung",
          desc: "대한민국의 최대 기업인 삼성에서도 저희에게 투자를 해주고 있습니다.",
          detail: "더보기",
        },
        {
          class: "t5",
          title: "Meta",
          desc: "얼마전에 이름을 facebook에서 바꾼 메타입니다.",
        },
        {
          class: "t6",
          title: "apple",
          desc: "애플에서도 저희에게 투자하고 있습니다.",
          detail: "더보기",
        },
      ],
      Texttitle: [
        {
          textTitle: "도움을 주신 모든 분들",
        },
      ],
    };
  },
};
</script>

<style>
#textType > h2 {
  color: #a6b8c4;
}
.text__inner {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}
.text {
  width: 32%;
  background: #f5f5f5;
  margin-bottom: 2%;
  padding: 20px;
  box-sizing: border-box;
  border-radius: 10px;
  transition: background 0.4s;
}
.text:hover {
  background: #a6c4b8;
}
.text__title {
  font-size: 24px;
  line-height: 1;
  white-space: nowrap;
  text-overflow: ellipsis;
  position: relative;
  padding-top: 75px;
  margin-bottom: 10px;
}
.text__title::before {
  content: "";
  position: absolute;
  left: 0;
  top: 0;
  width: 60px;
  height: 60px;
  border-radius: 50%;
  background: url(../../assets/img/text_icon.svg);
}
.text.t1 .text__title::before {
  background-position: 0 0;
}
.text.t2 .text__title::before {
  background-position: -60px 0;
}
.text.t3 .text__title::before {
  background-position: -120px 0;
}
.text.t4 .text__title::before {
  background-position: -180px 0;
}
.text.t5 .text__title::before {
  background-position: -240px 0;
}
.text.t6 .text__title::before {
  background-position: -300px 0;
}
.text__desc {
  font-size: 18px;
  font-weight: 300;
  line-height: 1.4;
  overflow: hidden;
  color: #666;
  margin-bottom: 20px;
  /* 세줄효과 추가 */
}
.text_btn {
  font-size: 16px;
  line-height: 1;
  text-decoration: underline;
  text-underline-position: under;
}
@media (max-width: 960px) {
  .text {
    width: 49%;
  }
}
@media (max-width: 600px) {
  .text__title {
    font-size: 20px;
  }
  .text__desc {
    font-size: 16px;
  }
}
@media (max-width: 480px) {
  .text {
    width: 100%;
  }
}
</style>
