<template src="./order.html"></template>

<script lang="ts">
import { Component, Prop,  Vue } from 'vue-property-decorator';
import Header from '../../components/header/Header.vue';
import Card from '../../components/card/Card.vue';
import OrderType from '../../types';
import './styles.scss';

@Component({
  components: {
     Header,
     Card,
    },
  })

export default class Order extends Vue {

    @Prop() private ordersNew!: OrderType[];
    @Prop() private ordersInProgress!: OrderType[];
    @Prop() private ordersWaiting!: OrderType[];
    @Prop() private ordersCompleted!: OrderType[];

  mounted(): void {
    document.title = "Orders";
  }
}
</script>
