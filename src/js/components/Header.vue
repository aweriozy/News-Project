<template>
  <div class="main-div">
    <div class="left-path">
      <h1 :class="{ shifted: isMenuOpen }">
        Работа мечты<br />
        компания Google
      </h1>
      <p :class="{ shifted: isMenuOpen }" class="first-p">
        Что из себя представляет работа в гугл?
      </p>
      <p :class="{ shifted: isMenuOpen }" class="second-p">
        Для многих людей Google представляется большим зданием с
        <br />прозрачными лоджиями и окнами от пола до потолка, которое<br />
        усеяно уютными и красивыми креслами/столами. От представления<br />
        кафетерия в этом здании, мечты становятся ещё красочнее,еда
        <br />пестрит излишествами и деликатесами и всё это бесплатно. <br />В
        окружении только доброжелательные, невероятно умные<br />
        и весёлые коллеги-друзья.Что же здесь правда?
      </p>
      <button type="button" :class="{ shifted: isMenuOpen }">
        ЧИТАТЬ ДАЛЕЕ
      </button>
    </div>
    <div :class="{ shifted: isMenuOpen }" class="right-path">
      <img src="/imgs/officegoogle.jpg" alt="office" />
    </div>
    <hr class="ended-first-block" />
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
.main-div {
  width: 100%;
  overflow: hidden;
}
.left-path {
  width: 890px;
  h1 {
    transition: transform 0.8s ease;
    margin-left: 100px;
    font-size: 3em;
    line-height: 1em;

    @media (max-width: 1024px) {
      font-size: 2.5em;
    }

    @media (max-width: 768px) {
      font-size: 2em;
    }

    @media (max-width: 439px) and (min-width: 320px) {
      font-size: 1.5em;
      margin-left: 20px;
      transform: translateX(0px);
    }
  }

  .first-p {
    text-transform: uppercase;
    margin-left: 100px;
    margin-top: 30px;
    font-size: 1.3em;
    color: #ababab;
    transition: transform 0.8s ease;
    @media (max-width: 1024px) {
      font-size: 1.2em;
      position: relative;
    }

    @media (max-width: 768px) {
      font-size: 1em;
    }
    @media (max-width: 590px) and (min-width: 440px) {
      font-size: 0.9em;
    }
    @media (max-width: 439px) and (min-width: 320px) {
      font-size: 0.8em;
      margin-left: 20px;
      transform: translateX(0px);
    }
  }

  .second-p {
    color: #ababab;
    font-size: 1.1em;
    margin-left: 100px;
    margin-top: 30px;
    transition: transform 0.8s ease;

    @media (max-width: 1024px) {
      font-size: 1em;
    }

    @media (max-width: 768px) {
      font-size: 0.9em;
    }
    @media (max-width: 590px) and (min-width: 510px) {
      font-size: 0.8em;
    }

    @media (max-width: 509px) and (min-width: 460px) {
      font-size: 0.7em;
    }

    @media (max-width: 459px) and (min-width: 320px) {
      font-size: 0.6em;
      margin-left: 20px;
      transform: translateX(0px);
    }
  }

  button {
    padding: 10px 15px;
    border-radius: 5px;
    border: 2px #5d98f8 solid;
    background-color: #fff;
    color: #5d98f8;
    font-size: 13px;
    font-weight: 600;
    cursor: pointer;
    margin-left: 100px;
    margin-top: 30px;
    transition: all 0.8s ease;

    &:hover {
      background-color: #ababab;
    }

    @media (max-width: 1024px) {
      padding: 6px 10px;
      font-size: 11px;
    }

    @media (max-width: 768px) {
      padding: 5px 8px;
      font-size: 10px;
    }

    @media (max-width: 439px) and (min-width: 320px) {
      margin-left: 20px;
      transform: translateX(0px);
    }
  }
}

button.shifted {
  transform: translateX(330px);

  @media (max-width: 439px) and (min-width: 320px) {
    transform: translateX(0px);
  }
}
.right-path {
  position: relative;
  width: 700px;
  height: 600px;
  left: 700px;
  top: -500px;
  overflow: hidden;

  img {
    width: 700px;
    height: auto;
    transition: scale 0.8s ease;

    @media (max-width: 1500px) and (min-width: 1430px) {
      width: 700px;
      height: auto;
    }

    @media (max-width: 1070px) and(min-width: 1030px) {
      width: 60%;
      height: 300px;
      position: relative;
      left: -100px;
      top: 100px;
    }

    @media (max-width: 1130px) and(min-width: 1071px) {
      width: 63%;
      height: 300px;
      position: relative;
      left: -100px;
      top: 100px;
    }
    @media (max-width: 1030px) {
      display: none;
    }
  }
}
.shifted.right-path img {
  scale: 0.8;
  transform: translateX(-150px);
}

.ended-first-block {
  border: 1px #ababab solid;
  position: relative;
  top: -500px;
  left: 80px;
  width: 90%;
  @media (max-width: 439px) and (min-width: 320px) {
    position: relative;
  }
}
.shifted {
  transform: translateX(250px) scale(0.8);
}

.left-path,
.right-path {
  transition: transform 0.8s ease, scale 0.8s ease;
}
</style>
