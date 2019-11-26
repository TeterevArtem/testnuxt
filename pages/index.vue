<template>
  <div class="container">
    <div class="row">
      <ul class="block__list col-lg-5">
        <li class="block__item">
          <h4 class="block__title">Мои счета</h4>
        </li>
        <li class="block__item">
          <h4 class="block__title">Мои счета</h4>
        </li>
        <li class="block__item">
          <h4 class="block__title">Мои счета</h4>
        </li>
        <li class="block__item">
          <h4 class="block__title">Мои счета</h4>
        </li>
      </ul>
      <ul class="block__list col-lg-5">
        <li class="block__item block__item_doc">
          <h4 class="block__title">Шаблоны операций</h4>
        </li>
        <li class="block__item block__item_doc">
          <h4 class="block__title">Шаблоны операций</h4>
        </li>
        <li class="block__item block__item_doc">
          <h4 class="block__title">Шаблоны операций</h4>
        </li>
        <li class="block__item block__item_doc">
          <h4 class="block__title">Шаблоны операций</h4>
        </li>
      </ul>
      <Sidebar/>
    </div>
  </div>
  
</template>

<script>
import Sidebar from "~/components/Sidebar"

export default {
  components:{
     Sidebar 
  }
}
</script>

<style lang="scss">
$red: #e3000f;
.block__list{
  list-style: none;
  margin: 0;
  padding: 0;    
}
.block__item{
  min-height: 370px;
  border: 1px solid #ffffff;
  border-radius: 5px;
  box-shadow: 0 0 3px rgba(0,0,0,.2);
  margin:0 25px 25px 0;
  position: relative;
  &:before{
    content: '';
    width: 30px;
    height: 60px;
    position: absolute;
    top: -4px;
    left: 8px;
    background: url("~assets/images/icons/case.png") center center no-repeat;
  }
  &_doc{
    &:before{
      background: url("~assets/images/icons/document.png") center center no-repeat;
    }
  }
  @media screen and(max-width: 992px){
    margin-right: 0
  }
}

.block__title{
  color: $red;
  border-bottom: 2px solid $red;
  margin-left: 50px;
  margin-top: 20px;
  margin-right: 10px;
  padding-bottom: 5px;
}


</style>

