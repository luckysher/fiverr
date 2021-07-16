<template src="./card.html"></template>

<script lang="ts">
    import { Component, Prop, Vue } from 'vue-property-decorator';
    import './styles.scss';

    @Component
    export default class Header extends Vue {

      @Prop() private order: any;

      private orderKey(): string {
        return "order_"+this.order.id;
      }

      private loadImage(name: string): string {
        return require('@/assets/img/'+name);
      }

      private loadCommentIcon(): string {
        return require('@/assets/img/comment_icon.png');
      }

      private loadUserIcon(): string {
        return require('@/assets/img/user.png');
      }

      private loadTimerIcon(): string {
        return require('@/assets/img/timer.png');
      }

    }
</script>
