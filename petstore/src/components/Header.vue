<template>
<header>
  <div class="navbar navbar-default">
    <div class="navbar-header">
      <h1><router-link :to="{name: 'iMain'}">{{ sitename }}</router-link></h1> <!-- iMain path로 연결 -->
    </div>
    <div class="nav navbar-nav navbar-right cart">
      <!-- <button type="button" class="btn btn-default btn-lg" v-on:click="showCheckout">
        <span class="glyphicon glyphicon-shopping-cart">{{cartItemCount}}</span> Check out
      </button> -->
      <router-link
          active-class="active"
          tag="button" class="btn btn-default btn-lg" :to="{name: 'Form'}">
        <span class="glyphicon glyphicon-shopping-cart">{{cartItemCount}}</span> Check out
      </router-link>
    </div>
  </div>
</header>
</template>

<script>
export default {
  name: 'my-header',
  data() {
    return {
      sitename: "Vue Pet-Shop"
    }
  },
  props: ['cartItemCount'],
  methods: {
    // showCheckout() {
    //   this.$router.push({name: 'Form'}); Form Path로 이동
    // }
  }
}
</script>

<style scoped>
a {
  text-decoration: none;
  color: black;
}
.router-link-exact-active {
  /* color: blue; */
  color: black;
}
</style>