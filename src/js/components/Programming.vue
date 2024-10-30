<template>
  <div class="programming">
    <hr :class="{ shifted: isMenuOpen }" class="first-line" />
    <div :class="{ shifted: isMenuOpen }" class="main-div">
      <div>
        <img src="/imgs/frontend.webp" alt="frontend" />
        <h1>Front-end</h1>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quia,
          perferendis
        </p>
        <button>Далее</button>
      </div>
      <div>
        <img src="/imgs/swift.jpg" alt="swift" />
        <h1>Swift</h1>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Libero,
          voluptas
        </p>
        <button>Далее</button>
      </div>
      <div>
        <img src="/imgs/python.png" alt="python" />
        <h1>Python</h1>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Explicabo,
          saepe
        </p>
        <button>Далее</button>
      </div>
      <div class="angular">
        <img src="/imgs/angular.webp" alt="angular" />
        <h1>Angular</h1>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nisi, minima
        </p>
        <button>Далее</button>
      </div>
      <div class="last-block">
        <img src="/imgs/phpmysql.jpg" alt="php" />
        <h1>PHP & MySQL</h1>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nisi, minima
        </p>
        <button>Далее</button>
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
.programming {
  margin-top: -110px;
  position: relative;

  .angular {
    @media (max-width: 1028px) and (min-width: 320px) {
      display: none;
    }
  }

  .last-block {
    @media (max-width: 1028px) and (min-width: 320px) {
      display: none;
    }
  }
}

.main-div {
  margin-top: 60px;
  display: flex;
  justify-content: space-around;
  margin-left: 10px;
  margin-right: 10px;

  h1 {
    margin-top: 10px;
    font-size: 1.7em;
    font-weight: 800;
  }

  p {
    margin-top: 20px;
    font-size: 1.05em;
    color: #ababab;

    @media (max-width: 658px) and (min-width: 320px) {
      display: none;
    }
  }

  button {
    padding: 12px 27px;
    border-radius: 5px;
    border: 2px #5d98f8 solid;
    background-color: #fff;
    color: #5d98f8;
    font-size: 13px;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.8s ease;
    margin-top: 20px;

    &:hover {
      background-color: #ababab;
    }

    @media (max-width: 658px) and (min-width: 320px) {
      margin-left: 25px;
    }
  }
}

.main-div > div {
  position: relative;
  width: 250px;
  @media (max-width: 658px) and (min-width: 320px) {
    margin-left: 50px;
  }

  img {
    width: 100%;
    height: 25vh;

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
}

.shifted {
  transform: translateX(180px) scale(0.7);
}

.shifted.first-line {
  transform: translateX(0px) translateY(-80px);
}

.shifted.main-div {
  transform: translateY(-150px) scale(0.7) translateX(180px);
}

.first-line {
  border: 1px #ababab solid;
  width: 90%;
  margin-top: 150px;
  margin-left: 80px;
}
</style>
