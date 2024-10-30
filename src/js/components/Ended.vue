<template>
  <div :class="{ shifted: isMenuOpen }" class="main-div">
    <div :class="{ shifted: isMenuOpen }" class="upper">
      <h1>Информация</h1>
    </div>
    <div :class="{ shifted: isMenuOpen }" class="lower">
      <div class="clients">
        <i class="fa-solid fa-people-group"></i>
        <div class="text">
          <h1>Множество клиентов</h1>
          <p>
            Огромное количество клиентов выбирают нас,<br />
            так как мы всегда держим руку на пульсе всего<br />
            происходящего.
          </p>
        </div>
      </div>
      <div class="youtube">
        <i class="fa-brands fa-youtube"></i>
        <div class="text">
          <h1>Большая аудитория YouTube</h1>
          <p>
            Большая фан база на площадке YouTube.<br />
            Вы всегда сможете найти ту информацию,<br />
            которая сейчас у всех на слуху на нашем канале.
          </p>
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
  data() {
    return {
      isVisible: false,
    };
  },
};
</script>
<style lang="scss" scoped>
.main-div {
  margin-top: 70px;
  margin-left: 80px;
  .upper {
    transition: all 600ms ease;
    h1 {
      font-size: 2.5em;
      font-weight: 600;
      border-bottom: 4px #5d98f8 solid;
      width: 265px;
    }
  }

  .lower {
    display: flex;
    margin-left: -20px;
    margin-top: 80px;
    justify-content: space-around;
    transition: all 600ms ease;

    .clients {
      display: flex;
      .text {
        margin-top: 20px;
      }

      i {
        color: #5d98f8;
        font-size: 2.8em;
        position: relative;
        top: 22px;
        margin-right: 20px;
      }
      h1 {
        font-size: 2em;
        font-weight: 800;
        line-height: 1em;
      }
      p {
        font-size: 1.1em;
        color: #ababab;
        margin-top: 20px;
      }
    }

    .youtube {
      display: flex;
      margin-left: 70px;
      .text {
        margin-top: 20px;
      }

      i {
        color: #5d98f8;
        font-size: 2.8em;
        position: relative;
        top: 22px;
        margin-right: 20px;
      }
      h1 {
        font-size: 2em;
        font-weight: 800;
        line-height: 1em;
      }
      p {
        font-size: 1.1em;
        color: #ababab;
        margin-top: 20px;
      }
    }
  }
}

.shifted {
  transform: translateX(180px) scale(0.7);
}

.shifted.main-div {
  transform: translateY(-210px);
  height: 30px;
}

.shifted.lower {
  transform: translateY(-80px) translateX(100px) scale(0.7);
}
</style>
