<template src="./order.html"></template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';
import './styles.scss';

@Component
export default class Order extends Vue {
  @Prop() private msg!: string;
}
</script>
