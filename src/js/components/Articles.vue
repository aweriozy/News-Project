<template>
  <div class="articles">
    <div class="container">
      <div class="title">
        <h1 :class="{ shifted: isMenuOpen }" class="fresh-news">
          Последние опубликованные
        </h1>
        <hr :class="{ shifted: isMenuOpen }" />
      </div>
      <div class="news">
        <div :class="{ shifted: isMenuOpen }" class="first">
          <div class="first_img">
            <img src="/imgs/first.jpg" alt="first_img" />
          </div>
          <h1>Какие языки программирования ненавидят больше и почему?</h1>
          <p>
            Авторитетный веб-ресурс Stack Overflow решил заняться опросом в
            отношении языков программирования. В этот раз в центре внимания
            нелюбимые языки.
          </p>
          <button>Далее</button>
        </div>
        <div :class="{ shifted: isMenuOpen }" class="second">
          <div class="second_img">
            <img src="/imgs/second.jpg" alt="second_img" />
          </div>
          <h1>Надо ли заклеивать камеру на ноутбуке?</h1>
          <p class="problematic-text">
            Заклеивать камеру ноутбука - паранойя или эффективное средство
            защититься от хакеров? Мы рассмотрим аспекты за и против и ответим
            на этот вездесущий вопрос.
          </p>
          <button class="problematic-btn">Далее</button>
        </div>
        <div :class="{ shifted: isMenuOpen }" class="third">
          <div class="third_img">
            <img src="/imgs/third.jpg" alt="third_img" />
          </div>
          <h1>5 будущих профессий для IT специалистов</h1>
          <p>
            Профессии постоянно пополняются и IT сфера вовсе не исключение. Мы
            подготовили список из 5 возможных профессий, к которым можно
            подготовиться уже сейчас.
          </p>
          <button>Далее</button>
        </div>
        <div :class="{ shifted: isMenuOpen }" class="fourth">
          <div class="fourth_img">
            <img src="/imgs/fourth.jpg" alt="fourth_img" />
          </div>
          <h1>ИИ на Python для распознавания голоса</h1>
          <p>
            На Python можно строить как простые программы, так и сложные ИИ
            системы. В данной статье мы покажем как реализовать распознание
            голоса и выполнение различных команд.
          </p>
          <button>Далее</button>
        </div>
        <div :class="{ shifted: isMenuOpen }" class="fifth">
          <div class="fifth_img">
            <img src="/imgs/fifth.webp" alt="fifth_img" />
          </div>
          <h1>Изучение Git на реальных примерах</h1>
          <p>
            Git - это очень полезная система управления версиями, которая
            позволяет разработчикам эффективнее работать вместе. В статье
            вкратце на примерах, вы изучите основные моменты Git.
          </p>
          <button>Далее</button>
        </div>
        <div :class="{ shifted: isMenuOpen }" class="sixth">
          <div class="sixth_img">
            <img src="/imgs/sixth.jpg" alt="sixth_img" />
          </div>
          <h1>Почему JavaScript очень крутой язык программирования?</h1>
          <p>
            Язык JS за последние года стал мега популярным и завоевал огромное
            доверие среди разработчиков. Почему он так крут? Узнаем в этой
            статье.
          </p>
          <button>Далее</button>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    isMenuOpen: {
      type: Boolean,
      default: false,
    },
  },
};
</script>
<style lang="scss" scoped>
.articles {
  position: relative;
  margin-top: -400px;
  .container {
    margin-left: 100px;
    .title {
      margin-top: 50px;
      width: 39%;
      .fresh-news {
        transition: transform 0.8s ease;
        font-size: 2em;
      }

      @media (max-width: 509px) and (min-width: 320px) {
        position: relative;
        left: -80px;
      }
      hr {
        height: 4px;
        background-color: #8ab4f8;
        width: 100%;
        border: none;
      }
    }

    .news {
      margin-left: -20px;
      margin-top: 50px;
      display: grid;
      grid-template-columns: 1fr 1fr;
      grid-template-rows: auto auto auto;
      gap: 20px;
      padding: 20px;
      position: relative;
      @media (max-width: 769px) and (min-width: 510px) {
        left: -30px;
      }

      @media (max-width: 509px) and (min-width: 320px) {
        margin-left: -100px;
      }

      img {
        width: 100%;
        cursor: pointer;
        opacity: 0.8;
        transition: all 600ms ease;
        overflow: hidden;
        transform: scale(1);

        &:hover {
          opacity: 1;
          transform: scale(1.1);
          overflow: hidden;
        }
      }

      h1 {
        font-size: 1.3em;
        font-weight: 600;
      }
      p {
        margin-top: 10px;
        font-size: 1.05em;
        color: #ababab;
      }

      button {
        padding: 12px 20px;
        border-radius: 5px;
        border: 2px #5d98f8 solid;
        background-color: #fff;
        color: #5d98f8;
        font-size: 13px;
        font-weight: 600;
        cursor: pointer;
        transition: all 0.8s ease;
        position: relative;
        top: 10px;
        margin-bottom: 20px;

        &:hover {
          background-color: #ababab;
        }
      }

      .first {
        img {
          @media (max-width: 1029px) and(min-width:770px) {
            width: 100%;
          }

          @media (max-width: 769px) and (min-width: 510px) {
            width: 30%;
          }

          @media (max-width: 510px) and(min-width:320px) {
            width: 30%;
          }
        }
        @media (max-width: 1500px) and(min-width:1030px) {
          width: 600px;
          padding: 20px;
        }

        @media (max-width: 1029px) and(min-width:770px) {
          width: 250px;
          overflow: hidden;
        }

        @media (max-width: 769px) and (min-width: 510px) {
          width: 180px;
          height: 60vh;
          overflow: hidden;
        }

        h1 {
          @media (max-width: 769px) and (min-width: 510px) {
            margin-top: -110px;
          }
          @media (max-width: 510px) and(min-width:320px) {
            margin-top: -110px;
          }
        }
        p {
          @media (max-width: 769px) and (min-width: 320px) {
            display: none;
          }
        }
        @media (max-width: 510px) and(min-width:320px) {
          width: 150px;
          overflow: hidden;
          height: 58vh;
          transform: translateX(0px);
        }
      }
      .second {
        .problematic-text {
          margin-top: 40px;
        }
        .problematic-btn {
          margin-top: 30px;
        }
        img {
          @media (max-width: 1029px) and(min-width:770px) {
            width: 100%;
          }

          @media (max-width: 769px) and (min-width: 510px) {
            width: 30%;
          }

          @media (max-width: 510px) and(min-width:320px) {
            width: 30%;
          }
        }
        @media (max-width: 1500px) and(min-width:1030px) {
          width: 600px;
          padding: 20px;
        }

        @media (max-width: 1029px) and(min-width:770px) {
          width: 250px;
          overflow: hidden;
        }

        @media (max-width: 769px) and (min-width: 510px) {
          width: 180px;
          height: 60vh;
          overflow: hidden;
        }
        @media (max-width: 510px) and(min-width:320px) {
          width: 150px;
          overflow: hidden;
          height: 58vh;
          transform: translateX(0px);
        }

        h1 {
          @media (max-width: 769px) and (min-width: 510px) {
            margin-top: -110px;
          }

          @media (max-width: 510px) and(min-width:320px) {
            margin-top: -110px;
          }
        }
        p {
          @media (max-width: 769px) and (min-width: 320px) {
            display: none;
          }
        }
      }
      .third {
        img {
          @media (max-width: 1029px) and(min-width:770px) {
            width: 100%;
          }

          @media (max-width: 769px) and (min-width: 510px) {
            width: 30%;
          }

          @media (max-width: 510px) and(min-width:320px) {
            width: 30%;
          }
        }
        @media (max-width: 1500px) and(min-width:1030px) {
          width: 600px;
          padding: 20px;
        }

        @media (max-width: 1029px) and(min-width:770px) {
          width: 250px;
          overflow: hidden;
        }

        @media (max-width: 769px) and (min-width: 510px) {
          width: 180px;
          height: 60vh;
          overflow: hidden;
        }
        @media (max-width: 510px) and(min-width:320px) {
          width: 150px;
          overflow: hidden;
          height: 58vh;
          transform: translateX(0px);
        }

        h1 {
          @media (max-width: 769px) and (min-width: 510px) {
            margin-top: -110px;
          }

          @media (max-width: 510px) and(min-width:320px) {
            margin-top: -110px;
          }
        }
        p {
          @media (max-width: 769px) and (min-width: 320px) {
            display: none;
          }
        }
      }
      .fourth {
        img {
          @media (max-width: 1029px) and(min-width:770px) {
            width: 100%;
          }

          @media (max-width: 769px) and (min-width: 510px) {
            width: 30%;
          }

          @media (max-width: 510px) and(min-width:320px) {
            width: 30%;
          }
        }
        @media (max-width: 1500px) and(min-width:1030px) {
          width: 600px;
          padding: 20px;
        }

        @media (max-width: 1029px) and(min-width:770px) {
          width: 250px;
          overflow: hidden;
        }

        @media (max-width: 769px) and (min-width: 510px) {
          width: 180px;
          height: 60vh;
          overflow: hidden;
        }
        @media (max-width: 510px) and(min-width:320px) {
          width: 150px;
          overflow: hidden;
          height: 58vh;
          transform: translateX(0px);
        }

        h1 {
          @media (max-width: 769px) and (min-width: 510px) {
            margin-top: -110px;
          }

          @media (max-width: 510px) and(min-width:320px) {
            margin-top: -110px;
          }
        }
        p {
          @media (max-width: 769px) and (min-width: 320px) {
            display: none;
          }
        }
      }
      .fifth {
        img {
          @media (max-width: 1029px) and(min-width:770px) {
            width: 100%;
          }

          @media (max-width: 769px) and (min-width: 510px) {
            width: 30%;
          }

          @media (max-width: 510px) and(min-width:320px) {
            width: 30%;
          }
        }
        @media (max-width: 1500px) and(min-width:1030px) {
          width: 600px;
          padding: 20px;
        }

        @media (max-width: 1029px) and(min-width:770px) {
          width: 250px;
          overflow: hidden;
        }

        @media (max-width: 769px) and (min-width: 510px) {
          width: 180px;
          height: 60vh;
          overflow: hidden;
        }
        @media (max-width: 510px) and(min-width:320px) {
          width: 150px;
          overflow: hidden;
          height: 58vh;
          transform: translateX(0px);
        }

        h1 {
          @media (max-width: 769px) and (min-width: 510px) {
            margin-top: -110px;
          }

          @media (max-width: 510px) and(min-width:320px) {
            margin-top: -110px;
          }
        }
        p {
          @media (max-width: 769px) and (min-width: 320px) {
            display: none;
          }
        }
      }
      .sixth {
        img {
          @media (max-width: 1029px) and(min-width:770px) {
            width: 100%;
          }

          @media (max-width: 769px) and (min-width: 510px) {
            width: 30%;
          }

          @media (max-width: 510px) and(min-width:320px) {
            width: 30%;
          }
        }
        @media (max-width: 1500px) and(min-width:1030px) {
          width: 600px;
          padding: 20px;
        }

        @media (max-width: 1029px) and(min-width:770px) {
          width: 250px;
          overflow: hidden;
        }

        @media (max-width: 769px) and (min-width: 510px) {
          width: 180px;
          height: 60vh;
          overflow: hidden;
        }
        @media (max-width: 510px) and(min-width:320px) {
          width: 150px;
          overflow: hidden;
          height: 58vh;
          transform: translateX(0px);
        }

        h1 {
          @media (max-width: 769px) and (min-width: 510px) {
            margin-top: -110px;
          }

          @media (max-width: 510px) and(min-width:320px) {
            margin-top: -110px;
          }
        }
        p {
          @media (max-width: 769px) and (min-width: 320px) {
            display: none;
          }
        }
      }
    }

    .news > div {
      background: #f9f9f9;
      width: 600px;
      padding: 20px;
      border-radius: 8px;
      box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
      transition: all 800ms ease;
    }

    .news > div > div {
      width: 600px;
      height: 211px;
      overflow: hidden;
    }
  }
}

.shifted {
  transform: translateX(250px) scale(0.7);
}

.first.shifted {
  scale: 0.9;
  margin-left: -20px;
  margin-top: -40px;
}

.second.shifted {
  scale: 0.9;
  margin-left: -100px;
  margin-top: -40px;
}
.third.shifted {
  scale: 0.9;
  margin-left: -20px;
  margin-top: -150px;
}
.fourth.shifted {
  scale: 0.9;
  margin-left: -100px;
  margin-top: -150px;
}
.fifth.shifted {
  scale: 0.9;
  margin-left: -20px;
  margin-top: -150px;
}
.sixth.shifted {
  scale: 0.9;
  margin-left: -100px;
  margin-top: -150px;
}

.last-line {
  border: 1px #ababab solid;
  width: 90%;
  margin-top: 100px;
  margin-left: 80px;
}
</style>
