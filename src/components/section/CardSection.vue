<template>
  <section id="cardType" class="card__wrap" :class="attr">
    <h2>SPACE PLANETS🐷</h2>
    <p>행성에 대해 자세히 배워가시면 더욱 도움이 될 것 입니다.</p>
    <div class="card__inner" :class="layout">
      <article class="card">
        <!-- 시멘틱 태그 다음에는 제목이 와야한다. 룰임; -->
        <figure class="card__header">
          <img src="../../assets/img/card_bg01.jpg" alt="행성" />
        </figure>
        <div class="card__body">
          <h3 class="tit">토성</h3>
          <p class="desc">
            토성 고리에는 엄청나게 많은 위성들이 있습니다, 그중에도 타이탄이라는
            위성에는 많은 석유를 매장하고 있다는 보고가 있습니다. 이자원들을
            활용...
          </p>
          <a class="btn" href="/">
            더 자세히 보기
            <span aria-hidden="true">
              <svg
                width="58"
                height="8"
                viewBox="0 0 58 8"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M57.3536 4.35355C57.5488 4.15829 57.5488 3.84171 57.3536 3.64645L54.1716 0.464466C53.9763 0.269204 53.6597 0.269204 53.4645 0.464466C53.2692 0.659728 53.2692 0.976311 53.4645 1.17157L56.2929 4L53.4645 6.82843C53.2692 7.02369 53.2692 7.34027 53.4645 7.53553C53.6597 7.7308 53.9763 7.7308 54.1716 7.53553L57.3536 4.35355ZM0 4.5H57V3.5H0V4.5Z"
                  fill="black"
                />
              </svg>
            </span>
          </a>
        </div>
      </article>
      <article class="card">
        <figure class="card__header">
          <img src="../../assets/img/card_bg02.jpg" alt="행성" />
        </figure>
        <div class="card__body">
          <h3 class="tit">해왕성</h3>
          <p class="desc">
            해왕성에는 수자원이 풍부해서 여러분들에게 충분한 물을 제공해 줄 수
            있습니다. 행성을 개발 할 수 있다면 지구에 물 부족은 존재하지 않을
            것입니다.
          </p>
          <a class="btn" href="/">
            더 자세히 보기
            <span aria-hidden="true">
              <svg
                width="58"
                height="8"
                viewBox="0 0 58 8"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M57.3536 4.35355C57.5488 4.15829 57.5488 3.84171 57.3536 3.64645L54.1716 0.464466C53.9763 0.269204 53.6597 0.269204 53.4645 0.464466C53.2692 0.659728 53.2692 0.976311 53.4645 1.17157L56.2929 4L53.4645 6.82843C53.2692 7.02369 53.2692 7.34027 53.4645 7.53553C53.6597 7.7308 53.9763 7.7308 54.1716 7.53553L57.3536 4.35355ZM0 4.5H57V3.5H0V4.5Z"
                  fill="black"
                />
              </svg>
            </span>
          </a>
        </div>
      </article>
      <article class="card">
        <figure class="card__header">
          <img src="../../assets/img/card_bg03.jpg" alt="행성" />
        </figure>
        <div class="card__body">
          <h3 class="tit">달</h3>
          <p class="desc">
            달에는 현재 심심치 않게 갈 수 있습니다. 여러분들은 달에 얼마나 많은
            양의 자원이 있는지 알고 있으십니다. 어떤 가치가 있는지 이야기를
            나눠보겠습니다.
          </p>
          <a class="btn" href="/">
            더 자세히 보기
            <span aria-hidden="true">
              <!-- 웹표준을 준수하기위해 보이스가 읽지 않도록 해줌 -->
              <svg
                width="58"
                height="8"
                viewBox="0 0 58 8"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M57.3536 4.35355C57.5488 4.15829 57.5488 3.84171 57.3536 3.64645L54.1716 0.464466C53.9763 0.269204 53.6597 0.269204 53.4645 0.464466C53.2692 0.659728 53.2692 0.976311 53.4645 1.17157L56.2929 4L53.4645 6.82843C53.2692 7.02369 53.2692 7.34027 53.4645 7.53553C53.6597 7.7308 53.9763 7.7308 54.1716 7.53553L57.3536 4.35355ZM0 4.5H57V3.5H0V4.5Z"
                  fill="black"
                />
              </svg>
            </span>
          </a>
        </div>
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
/* cardType */
#cardType > h2 {
  color: #fff;
}
#cardType > p {
  color: #a4b8c4;
}

.card__inner {
  display: flex;
  justify-content: space-between;
  /* 비율에 알맞게 정렬 시켜주는 코드 */
}
.card {
  width: 32%;
  background: #f5f5f5;
  border-radius: 20px;
}
.card__header img {
  border-top-left-radius: 20px;
  border-top-right-radius: 20px;
}

.card__body {
  padding: 24px;
}
.card__body:hover {
  background: #a4c4b8;
}

.card__body .tit {
  font-size: 24px;
  margin-bottom: 10px;
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
  padding-right: 20px;
}

.card__body .desc {
  font-size: 18px;
  margin-bottom: 20px;
  line-height: 1.4;
  color: #666;
  font-weight: 300;
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 4;
  -webkit-box-orient: vertical;
}

@media (max-width: 960px) {
  .card__inner {
    flex-wrap: wrap;
  }
  .card {
    width: 49%;
  }
  .card:last-child {
    display: none;
  }
}
@media (max-width: 600px) {
  .card {
    width: 100%;
  }
  .card:first-child {
    margin-bottom: 20px;
  }
  .card__body {
    padding: 20px;
  }
  .card__body .desc {
    font-size: 16px;
  }
}
</style>
