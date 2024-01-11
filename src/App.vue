<script>
import AppHeader from './components/AppHeader.vue';
import ProductList from './components/ProductList.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  components: {
    AppHeader,
    ProductList,
    AppFooter,
  }
}
</script>

<template>
  <AppHeader />
  <main>
    <ListProducts />
  </main>
  <AppFooter />
</template>

<style lang="scss">
@use './styles/general.scss' as *;
@use './styles/partials/variables' as *;

a {
  color: $grey;
}
</style>