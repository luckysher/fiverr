<template>
  <div id="app">
     <Order
        v-bind:ordersNew="orders"
        v-bind:ordersInProgress="orders"
        v-bind:ordersWaiting="orders"
        v-bind:ordersCompleted="orders" />
  </div>
</template>

<script lang="ts">
    import { Component, Vue } from 'vue-property-decorator';
    import './assets/css/global-styles.scss';
    import Order from './pages/orders/Order.vue';
    import OrderType from './types';

    @Component({
      components: {
        Order,
      },
    })
    export default class App extends Vue {
        private data = [{
            id: '1',
            title: 'jug',
            image_name: 'jug.jpg',
            days: '5 days left',
            hours: '5 hrs',
            cost: '$32',
            status: 'New Order'
          },
          {
            id: '1',
            title: 'jug',
            image_name: 'jug.jpg',
            days: '5 days left',
            hours: '5 hrs',
            cost: '$32',
            status: 'New Order'
          }];

        get orders(): OrderType[] {
            return this.data;
        }
    }
</script>

