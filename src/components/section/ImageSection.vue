<template>
  <section
    id="imageType"
    class="image__wrap"
    :class="attr"
    v-for="header in header"
    :key="header"
  >
    <h2>{{ header.header }}</h2>
    <p>{{ header.subtitle }}</p>
    <div class="image__inner" :class="layout">
      <article
        class="image"
        :class="title.class"
        v-for="title in title"
        :key="title"
      >
        <h3 class="image__title">{{ title.text }}</h3>
        <p class="image__desc">{{ title.desc }}</p>
        <a href="#">{{ title.detail }}</a>
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
  data() {
    return {
      header: [
        {
          header: "μ°μ£Όπ",
          subtitle:
            "μ°μ£Όλ λμ΄μ κ° μ μλ μμ­μ΄ μλλλ€. μ ν¬κ° λμλλ¦¬κ² μ΅λλ€.",
        },
      ],
      title: [
        {
          text: "λ¬ νλ‘μ νΈ",
          desc: "λ¬μμ μ§ννλ μ¬μμ λν μ΄μΌκΈ°λ₯Ό λλ λ³΄λλ‘ νκ² μ΅λλ€. λ¬μ μ§κΈλ κ°λ°νκ³  μμ΅λλ€ μ ν¬λ μλλ³΄λ€ μμ κ°κΈ°μν΄μ...",
          class: "img1",
          detail: "μμΈνλ³΄κΈ°",
        },
        {
          text: "μν νλ‘μ νΈ",
          desc: "  μ°λ¦¬ μνκ³κ° μΌλ§λ λ§μ μμμ κ°μ§κ³  μλμ§ μκ³  μμΌμ­λκΉ? μνκ³λ μμ²­λ κ°μΉλ₯Ό μ§λκ³  μκ³  νμ¬λ₯Ό μν΄ μ¬λ¬λΆμ λμμ΄ νμν©λλ€.",
          class: "img2",
          detail: "μμΈνλ³΄κΈ°",
        },
      ],
    };
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
