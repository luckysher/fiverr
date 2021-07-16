<template src="./order.html"></template>

<script lang="ts">
import { Component, Prop,  Vue } from 'vue-property-decorator';
import Header from '../../components/header/Header.vue';
import Card from '../../components/card/Card.vue';
import './styles.scss';

@Component({
  components: {
     Header,
     Card,
    },
  })
export default class Order extends Vue {

  @Prop() private ordersNew = [{
        id: '1',
        title: 'jug',
        image_name: 'jug.jpg',
        days: '5 days left',
        hours: '5 hrs',
        cost: '$32',
        status: 'New Order'
      },
      {
        id: '2',
        title: 'jug',
        image_name: 'jug.jpg',
        days: '6 days left',
        hours: '3 hrs',
        cost: '$52',
        status: 'New Order'
      }];

  @Prop() private ordersInProgress = [{
        id: '1',
        title: 'jug',
        image_name: 'jug.jpg',
        days: '5 days left',
        hours: '5 hrs',
        cost: '$32',
        status: 'New Order'
      },
      {
        id: '2',
        title: 'jug',
        image_name: 'jug.jpg',
        days: '6 days left',
        hours: '3 hrs',
        cost: '$52',
        status: 'New Order'
      }];

    @Prop() private ordersWaiting = [{
        id: '1',
        title: 'jug',
        image_name: 'jug.jpg',
        days: '5 days left',
        hours: '5 hrs',
        cost: '$32',
        status: 'New Order'
      },
      {
        id: '2',
        title: 'jug',
        image_name: 'jug.jpg',
        days: '6 days left',
        hours: '3 hrs',
        cost: '$52',
        status: 'New Order'
      }];

    @Prop() private ordersCompleted = [{
        id: '1',
        title: 'jug',
        image_name: 'jug.jpg',
        days: '5 days left',
        hours: '5 hrs',
        cost: '$32',
        status: 'New Order'
      },
      {
        id: '2',
        title: 'jug',
        image_name: 'jug.jpg',
        days: '6 days left',
        hours: '3 hrs',
        cost: '$52',
        status: 'New Order'
      }];

  // On page mount
  mounted(): void {
    document.title = "Orders";
  }
}
</script>
