<template src="./order.html"></template>

<script lang="ts">
import { Component,  Vue } from 'vue-property-decorator';
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

  // On page mount
  mounted(): void {
    document.title = "Orders";
  }

}
</script>
