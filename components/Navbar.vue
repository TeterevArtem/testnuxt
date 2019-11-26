<template>
    <nav class="navbar navbar-expand-lg navbar-light col-12">
      <a class="navbar-brand" href="#"></a>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav mr-auto col-12">
          <li class="nav-item">
            <nuxt-link class="nav-link" active-class="active" exact no-prefetch to="/">Главная <span class="sr-only">(current)</span></nuxt-link>
          </li>
          <li class="nav-item">
            <nuxt-link class="nav-link"  active-class="active" to="/about">О Нас</nuxt-link>
          </li>
          <li class="nav-item">
            <nuxt-link class="nav-link"  active-class="active" to="/contacts">Контакты</nuxt-link>
          </li>
          <li class="nav-item">
            <nuxt-link class="nav-link" to="#" disabled>Платежи</nuxt-link>
          </li>
          <li class="nav-item">
            <nuxt-link class="nav-link" to="#" disabled>Купля/Продажа валют</nuxt-link>
          </li>
          <li class="nav-item">
            <nuxt-link class="nav-link" to="#" disabled>Заявки</nuxt-link>
          </li>
          <li class="nav-item">
            <nuxt-link class="nav-link" to="#" disabled>Наши Контакты</nuxt-link>
          </li>
        </ul>
      </div>
    </nav>
</template>



<style lang="scss">
.navbar{
  background: linear-gradient(to bottom, #fff, #d9d9d9);
  border-radius: 5px;
  font-size: 13px;
}
.navbar-nav{
  justify-content: space-between;
  padding: 0px
}
.nav-item{
  text-align: center;
  padding: 0 20px;
  .active{
    background: radial-gradient(ellipse at 50% 100%,#fff, transparent);
  }
  &:last-child{
    border-right: 0
  }
}
</style>