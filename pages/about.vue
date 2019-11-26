<template>
  <div>
    <h2 class="page__title">{{pageTitle}}</h2>
    <div class="user__info">
      <ul class="user__list">
        <li class="user__item" v-for="user of users" :key="user.id">{{user.name}}</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    pageTitle: 'Users page',
    users: []
  }),
  async mounted(){
    this.users = await this.$axios.$get('https://jsonplaceholder.typicode.com/users')
  }
}
</script>

<style lang="scss">
$red: #e3000f;
.page__title{
  color: $red;
  padding-bottom: 10px;
  border-bottom: 2px solid $red;
}

.user__list{
  list-style: none;
  margin: 0;
  padding: 0;
  border: 1px solid #ffffff;
  border-radius: 5px;
  box-shadow: 0 0 2px rgba(0,0,0,.3); 
}

.user__item{
  margin: 10px 0;
  padding-left: 20px;
}
</style>