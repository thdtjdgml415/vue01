<template>
  <section id="imgtextType" class="imgText__wrap" :class="attr">
    <h2 class="blind">유용한 사이트 살펴보기</h2>
    <div class="imgText__inner" :class="layout">
      <div
        class="imgText__txt"
        v-for="imgtextType in imgtextType"
        :key="imgtextType"
      >
        <span>{{ imgtextType.title }}</span>
        <h3>{{ imgtextType.title2 }}</h3>
        <p>{{ imgtextType.desc }}</p>
        <ul>
          <li>
            <a href="/">{{ imgtextType.list }}</a>
          </li>
          <li>
            <a href="/">{{ imgtextType.list2 }}</a>
          </li>
          <li>
            <a href="/">{{ imgtextType.list3 }}</a>
          </li>
          <li>
            <a href="/">{{ imgtextType.list4 }}</a>
          </li>
          <li>
            <a href="/">{{ imgtextType.list5 }}</a>
          </li>
          <li>
            <a href="/">{{ imgtextType.list6 }}</a>
          </li>
        </ul>
      </div>
      <div class="imgText__img" :class="imgarticle[0].image">
        <a href="/">{{ imgarticle[0].desc }}</a>
      </div>
      <div class="imgText__img" :class="imgarticle[1].image">
        <a href="/" class="blue">{{ imgarticle[1].desc }}</a>
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
      imgtextType: [
        {
          title: "우주에 관한 사이트",
          title2: "Space reference",
          desc: "우주산업에 투자해보세요!",
          list: "튜토리얼 사이트",
          list2: "레퍼런스 사이트",
          list3: "space 사이트",
          list4: "twitter 사이트",
          list5: "spaceX 사이트",
          list6: "Youtube사이트",
        },
      ],
      imgarticle: [
        {
          image: "img1",
          desc: "레퍼런스 사이트",
        },
        {
          image: "img2",
          desc: "튜토리얼 사이트",
        },
      ],
    };
  },
};
</script>

<style>
/* imgtextType */
.imgText__inner {
  display: flex;
  justify-content: space-between;
  background-color: #202020;
}

.imgText__inner > div {
  width: 32%;
  height: 500px;
}

.imgText__txt span {
  font-size: 16px;
  color: #a6b8c4;
  text-decoration: underline;
  text-underline-position: under;
  margin-bottom: 20px;
  display: block;
}
.imgText__txt h3 {
  font-size: 50px;
  font-weight: 500;
  margin-bottom: 20px;
  color: #fff;
}
.imgText__txt p {
  font-size: 18px;
  font-weight: 300;
  line-height: 1.5;
  color: #a6b8c4;
  margin-bottom: 10px;
}
.imgText__txt ul {
  font-size: 18px;
  font-weight: 300;
  line-height: 1.6;
}
.imgText__txt ul li {
  position: relative;
  padding-left: 20px;
}
.imgText__txt ul li a {
  color: #a6b8c4;
}
.imgText__txt ul li:before {
  content: "";
  width: 5px;
  height: 5px;
  border-radius: 50%;
  position: absolute;
  left: 5px;
  top: 9px;
  background: #666;
}
.imgText__img {
  position: relative;
  border-radius: 20px;
}
.imgText__img a {
  position: absolute;
  left: 30px;
  bottom: 30px;
  color: #fff;
  background-color: #7c2b39;
  font-size: 18px;
  padding: 10px 30px;
  border-radius: 30px;
  display: inline-block;
}
.imgText__img a.blue {
  background-color: #2b387c;
}
.imgText__img.img1 {
  background: url(../../assets/img/Roket.jpg) no-repeat center / cover;
}
.imgText__img.img2 {
  background: url(../../assets/img/Rocket2.jpg) no-repeat center / cover;
}
@media (max-width: 960px) {
  .imgText__inner {
    flex-wrap: wrap;
  }
  .imgText__txt h3 {
    font-size: 30px;
  }
  .imgText__txt p {
    margin-bottom: 60px;
  }
  .imgText__inner > div.imgText__txt {
    width: 100%;
    height: auto;
    text-align: center;
  }
  .imgText__inner > div.imgText__txt ul {
    display: none;
  }
  .imgText__inner > div.imgText__img {
    width: 50%;
  }
}
@media (max-width: 600px) {
  .imgText__txt span {
    font-size: 14px;
    margin-bottom: 10px;
  }
  .imgText__txt h3 {
    font-size: 30px;
  }
  .imgText__txt p {
    margin-bottom: 50px;
    font-size: 16px;
  }
  .imgText__inner > div.imgText__img {
    width: 100%;
    height: 200px;
  }
  .imgText__inner > div.imgText__img.img1 {
    margin-bottom: 20px;
  }
  .imgText__img a {
    left: 20px;
    bottom: 20px;
  }
}
</style>
