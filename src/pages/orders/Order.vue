<template src="./order.html"></template>

<script lang="ts">
import { Component,  Vue } from 'vue-property-decorator';
import './styles.scss';
import Header from '../../components/header/Header.vue';

@Component({
  components: {
     Header,
    },
  })
export default class Order extends Vue {

  // On page mount
  mounted(): void {
    document.title = "Orders";
  }

}
</script>
