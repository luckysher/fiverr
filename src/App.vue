<template>
  <div id="app">
     <Order />
  </div>
</template>

<script lang="ts">
    import { Component, Vue } from 'vue-property-decorator';
    import './assets/css/global-styles.scss';
    import Order from './pages/orders/Order.vue';

    @Component({
      components: {
        Order,
      },
    })
    export default class App extends Vue {}
</script>

