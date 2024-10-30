<template>
  <div id="app">
    <div class="general">
      <i v-if="!isMenuOpen" class="fa-solid fa-bars" @click="toggleMenu"></i>

      <transition name="slide">
        <div v-if="isMenuOpen" class="open-menu">
          <i class="fa-solid fa-x close-icon" @click="toggleMenu"></i>

          <input type="text" placeholder="Поиск" />
          <h1>Меню</h1>
          <a href="#!">Главная</a>
          <a href="#!">Про нас</a>
          <a href="#!">Контакты</a>
          <div class="circumcision">
            <h2>Информация про нас</h2>
            <hr class="menu-line" />
            <img
              src="/imgs/male-programmer-is-writing-program-code-laptop-home_97716-1206.avif"
              alt="programmist"
              class="first-img"
            />
            <p class="first-text">
              На днях был придуман новый язык программирования - Kotik!
            </p>
            <hr class="last-line" />
            <img class="second-img" src="/imgs/sobes.jpg" alt="sobes" />
            <p class="second-text">
              Эксперты усомнились в подлинности данных, которые предоставила
              компания Apple
            </p>
            <button type="button">Далее</button>
            <h1 class="help">Помощь</h1>
            <p class="if-need-help">
              Если у вас возникли какие-либо вопросы и вы хотите связаться с
              нами для уточнения всех моментов, то ниже представлены все
              контактные данные для связи с нами.
            </p>
            <div class="contact-block">
              <div class="email">
                <i class="fa-regular fa-envelope"></i>
                <p>test@itproger.com</p>
              </div>
              <hr />
              <div class="phone">
                <i class="fa-solid fa-phone"></i>
                <p>(000)000 - 0000</p>
              </div>
              <hr />
              <div class="address">
                <i class="fa-solid fa-map-location-dot"></i>
                <p>USA Washington Seattle Northway 13002</p>
              </div>
              <p class="final-text">
                Все права защищены &copy;. При использовании данных указывайте
                ссылку на первоисточник
              </p>
            </div>
          </div>
        </div>
      </transition>

      <div
        :class="{ 'main-content': true, 'main-content-shrinked': isMenuOpen }"
      >
        <h1 class="title">СМИ портал</h1>
      </div>
      <hr :class="{ shifted: isMenuOpen }" class="custom-line" />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isMenuOpen: false,
    };
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen;
      this.$emit("menu-toggle", this.isMenuOpen); // Отправка события в App.vue
    },
  },
};
</script>

<style lang="scss" scoped>
#app {
  position: relative;
  transition: all 800ms ease;
  overflow: hidden;
}

i {
  margin: 20px 40px;
  font-size: 25px;
  color: #198cff;
  cursor: pointer;
  transition: all 800ms ease;
}

.main-content {
  transition: scale 800ms ease;
  transition: all 800ms ease;
  @media (max-width: 439px) and (min-width: 320px) {
    transform: translateX(0px);
  }
}

.main-content-shrinked {
  transform: translateX(250px) scale(0.9);
  transition: all 800ms ease;

  @media (max-width: 439px) and (min-width: 320px) {
    transform: translateX(0px);
  }
}

.open-menu {
  position: fixed;
  top: 0;
  left: 0;
  width: 300px;
  height: 100%;
  background-color: white;
  border-right: 1px solid #ccc;
  padding: 20px;
  box-shadow: 4px 0 8px rgba(0, 0, 0, 0.1);
  display: flex;
  flex-direction: column;
  overflow-y: auto;
  z-index: 1000;

  @media (max-width: 1024px) and (min-width: 768px) {
    width: 300px;
  }

  @media (max-width: 767px) {
    width: 200px;
    height: auto;
  }

  @media (max-width: 439px) and (min-width: 320px) {
    opacity: 0.9;
  }
}

.close-icon {
  align-self: flex-end;
  font-size: 20px;
  cursor: pointer;
  color: #198cff;
  margin-bottom: 20px;
  transition: all 800ms ease;
}

.open-menu input {
  margin-bottom: 10px;
  transition: all 800ms ease;
  border-radius: 5px;
  border: 2px solid #8ab4f8;
  padding: 10px 20px;
  cursor: pointer;

  &:hover {
    -webkit-box-shadow: 4px 4px 15px 10px rgba(45, 45, 45, 0.2);
    -moz-box-shadow: 4px 4px 15px 10px rgba(45, 45, 45, 0.2);
    box-shadow: 4px 4px 15px 10px rgba(45, 45, 45, 0.2);
  }
}

.open-menu h1 {
  margin: 20px 0 0 0;
  padding-bottom: 10px;
  transition: all 800ms ease;
  border-bottom: 3px solid #8ab4f8;
  display: inline-block;
  font-size: 2em;
  width: 95px;
  height: 35px;
}

.open-menu a {
  margin: 10px 0;
  margin-top: 15px;
  color: #363636;
  text-decoration: none;
  transition: all 800ms ease;
  //   border-bottom: 3px solid #8ab4f8;
  width: 75px;

  &:hover {
    color: #198cff;
    background-color: rgba(45, 45, 45, 0.2);
    -webkit-box-shadow: 4px 4px 15px 10px rgba(131, 232, 243, 0.2) inset;
    -moz-box-shadow: 4px 4px 15px 10px rgba(131, 232, 243, 0.2) inset;
    box-shadow: 4px 4px 15px 10px rgba(131, 232, 243, 0.2) inset;
    border-radius: 5px;
  }
}

.slide-enter-active,
.slide-leave-active {
  transition: all 800ms ease;
}

.slide-enter-from {
  transform: translateX(-100%);
  transition: all 800ms ease;
}

.slide-leave-to {
  transform: translateX(-100%);
  transition: all 800ms ease;
}

.open-menu h2 {
  margin-top: 20px;
}

.title {
  position: relative;
  top: -50px;
  left: 30px;
  margin: 50px;
  width: 192px;
  transition: all 800ms ease;

  @media (max-width: 1024px) and (min-width: 768px) {
    margin-left: 120px;
  }

  @media (max-width: 767px) {
    margin-left: 120px;
  }

  @media (max-width: 439px) and (min-width: 320px) {
    margin-left: -10px;
  }
}

.custom-line {
  width: 90%;
  height: 4px;
  background-color: #8ab4f8;
  border: none;
  position: relative;
  left: 30px;
  margin: 50px;
  top: -85px;
  transition: all 800ms ease;
  overflow: hidden;

  @media (max-width: 1024px) and (min-width: 768px) {
    width: 80%;
    margin-left: 70px;
  }

  @media (max-width: 767px) {
    width: 70%;
    margin-left: 70px;
  }
  @media (max-width: 439px) and (min-width: 320px) {
    margin-left: -10px;
  }
}

.first-text {
  font-size: 0.9em;
  font-weight: 600;
  color: #504646;
  margin-top: 10px;
}

.last-line {
  height: 2px;
  width: 320px;
  background-color: #808080;
  border: none;
  margin-top: 15px;
}

.menu-line {
  width: 90%;
  height: 4px;
  background-color: #8ab4f8;
  border: none;
}

.first-img {
  margin-top: 25px;
  height: 20vh;
  width: 320px;
}

.second-img {
  margin-top: 25px;
  height: 20vh;
  width: 320px;
}

.second-text {
  font-size: 0.9em;
  font-weight: 600;
  color: #504646;
  margin-top: 10px;
}

button {
  padding: 10px 20px;
  width: 100px;
  margin-top: 20px;
  border-radius: 5px;
  border: 2px #5d98f8 solid;
  background-color: #fff;
  color: #5d98f8;
  font-size: 13px;
  font-weight: 600;
  cursor: pointer;
  transition: all 0.8s ease;
  margin-bottom: 50px;
  display: block;

  &:hover {
    background-color: #ababab;
  }
}

.help {
  transition: all 800ms ease;
  border-bottom: 3px solid #8ab4f8;
  display: inline-block;
  font-size: 2em;
  width: 95px;
  height: 35px;
  margin-top: 20px;
}

.if-need-help {
  font-size: 0.9em;
  font-weight: 600;
  color: #504646;
  margin-top: 40px;
}

.open-menu {
  .circumcision {
    @media (max-width: 760px) {
      display: none;
    }
  }
  .contact-block {
    .email {
      display: flex;
      margin-top: 30px;

      p {
        font-size: 0.9em;
        margin-top: 20px;
      }
    }

    .phone {
      display: flex;
      p {
        margin-top: 20px;
        font-size: 0.9em;
      }
    }
    .address {
      display: flex;

      p {
        font-size: 0.9em;
        margin-top: 20px;
      }
    }
    hr {
      margin: 10px 0;
    }
    .final-text {
      margin-top: 50px;
      margin-bottom: 50px;
      color: #ababab;
    }
  }
}
</style>
