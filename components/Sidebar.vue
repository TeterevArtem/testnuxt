<template>
  <ul class="sidebar__list col-lg-2">
    <li class="sidebar__item">
      <h5 class="sidevar__title">Курс обмена валют:</h5>
    </li>
    <li class="sidebar__item">
      <div class="sidebar__image sidebar__image_auto"></div>
      <h5 class="sidevar__title sidevar__title_red">Кредит Auto</h5>
    </li>
    <li class="sidebar__item">
      <div class="sidebar__image sidebar__image_dep"></div>
      <h5 class="sidevar__title sidevar__title_red">Депозиты</h5>            
    </li>
  </ul>
</template>

<style lang="scss">
$red: #e3000f;
.sidebar__list{
  list-style: none;
  margin: 0;
  padding: 0;
  @media screen and(max-width: 992px){
    display: none;
  }
}

.sidebar__item{
  min-height: 205px;
  border-radius: 5px;
  border: 1px solid #fff;
  margin-bottom: 30px;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.sidebar__image{
  min-height: 170px;
  background-size: cover;
}
.sidebar__image_auto{
  background-image: url("~assets/images/auto.png");
  background-position: center center;
}
.sidebar__image_dep{
  background-image: url("~assets/images/deposits.png");
  background-position: center center;
}
.sidevar__title{
  font-size: 13px;
  margin-top: 10px;
  padding-left: 10px;
  &_red{
    background: $red;
    color: #fff;
    font-size: 12px;
    padding: 10px;
    margin: 0;
  }
}
</style>