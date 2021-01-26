<template>
  <div id="app">
    <header>
      <div class="line"></div>
      <div class="header-bar container">
        <div class="header-bar__left">
          <app-button>Перейти в личный кабинет</app-button>
          <app-button dropable>RU</app-button>
        </div>
        <div class="header-bar__right">
          <app-button>Login</app-button>
          <app-button type="primary">Register</app-button>
          <app-button><img src="./assets/img/menu-icon.png" alt="menu-icon"></app-button>
        </div>
      </div>
    </header>

    <main class="main">
      <div class="block1">
        <h3 class="main-title">What are the fees?</h3>
        <p>
          Bank fee for organizing the transaction is fixed, <span class="active-color">amounts to 0.08%</span>, does not
          <br>
          depend on the timing and is included in the interest on the loan rate
        </p>
      </div>
      <div class="block2">
        <div class="block2__content container">
          <h3 class="secondary-title">What’s next?</h3>
          <img src="./assets/img/arrow-next.png" alt="next" class="next-arrow">
          <a href="#" class="link">Top up wallet using Exchange service</a>
          <img src="./assets/img/arrow-next.png" alt="next" class="next-arrow">
          <a href="#" class="link">Join the investor club</a>
          <img src="./assets/img/arrow-next.png" alt="next" class="next-arrow">
          <a href="#" class="link">Open Holder account</a>
        </div>
      </div>
      <div class="block3">
        <div class="block3__content container">
          <div class="block3__title">
            <h3 class="main-title">Empty Company</h3>
            <span style="margin-left: 25px">
              <img src="./assets/img/converse.png" alt="">
              <a href="" class="secondary-link">Обратная связь</a>
            </span>
          </div>
          <div class="block3__info">
            <div class="block3__info__item">
              Company Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent porttitor ornare neque, non elementum sapien gravida sit amet. Ut ac convallis arcu, sit amet
            </div>
            <div class="block3__info__item">
              Company Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent porttitor ornare neque, non elementum sapien gravida sit amet. Ut ac convallis arcu, sit amet
            </div>
            <div class="block3__info__item">
              Company Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent porttitor ornare neque, non elementum sapien gravida sit amet. Ut ac convallis arcu, sit amet
            </div>
          </div>

        </div>
      </div>
    </main>

    <footer class="footer">
      <ul class="footer__content container">
        <li class="footer__item">Infrastructure</li>
        <li class="footer__item">Terms of use</li>
        <li class="footer__item">Privacy policy</li>
        <li class="footer__item">KYC/AML policy</li>
        <li class="footer__item">Information center</li>
        <li class="footer__item">Roadmap</li>
      </ul>
    </footer>
  </div>
</template>

<script>
import AppButton from "./components/AppButton";
export default {
  name: 'App',
  components: {AppButton}
}
</script>

<style lang="less">
/* header */
.header-bar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 125px;
}

/* main */
main {
  display: grid;
  grid-template-rows: 1fr 160px 250px;
}
.block1 {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-around;
  padding: 100px;
}
.block2 {
  background: linear-gradient(180deg, #55BCFC 0%, #3D75F1 100%);
  &__content {
    display: flex;
    align-items: center;
    height: 100%;
  }
}
.block3 {
  background-color: #fff;
  &__content {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: space-around;
    height: 100%;
  }
  &__title {
    display: flex;
    flex-direction: row;
  }
  &__info {
    display: grid;
    width: 100%;
    text-align: start;
    grid-gap: 3px;
    grid-template-columns: 1fr 1fr 1fr;
    &__item {
      border-left: 2px solid #3D75F2;;
      padding: 0 20px 20px;
      color: #000;
    }
  }
}

/* footer */
.footer {
  background: linear-gradient(270.16deg, #55BCFC 0%, #3D75F1 100%);
  height: 100px;
  color: #fff;
  &__content {
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 100px;
    flex-wrap: wrap;
  }
  &__item { cursor: pointer; }
}


</style>

