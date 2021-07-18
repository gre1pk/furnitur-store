<template>
  <header class="page-header">
    <div class="header-top conteiner">
      <label for="">label </label>
      <ul class="header-top__list">
        <li class="header-top__account">Мой профиль</li>
        <li class="header-top__liks">Избранное :</li>
        <li class="header-top__cart">Ваша карзина :</li>
      </ul>
    </div>
    <div class="header-bottom">
      <nav class="main-nav conteiner">
        <ul class="main-nav__list">
          <li class="main-nav__item">
            <router-link to="/">Главная</router-link>
          </li>
          <li class="main-nav__item">
            <router-link to="/">Список товаров</router-link>
          </li>
          <li class="main-nav__item">
            <router-link to="/">Ремонт мебели</router-link>
          </li>
        </ul>
        <router-view />
        <div class="main-nav__search">Поиск</div>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style lang="scss">
@import "@/assets/scss/index.scss";
.page-header {
  display: flex;
  flex-direction: column;
}
.header-top {
  display: flex;
  justify-content: space-between;
  background-color: #ffff;
  align-items: center;
  height: 150px;

  &__list {
    display: flex;
    justify-content: space-between;
    width: 450px;
  }
}
.header-bottom {
  background-color: #333333;
  height: 90px;
  padding-top: 20px;
}
.main-nav {
  background-color: #ffffff;
  display: flex;
  justify-content: space-between;
  height: 50px;
  box-shadow: 0px 4px 20px 2px rgba(0, 0, 0, 0.02);
  border-radius: 5px;

  &__list {
    display: flex;
    justify-content: space-between;
  }
}
</style>
