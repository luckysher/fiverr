<template src="./header.html"></template>

<script lang="ts">
    import { Component, Prop, Vue } from 'vue-property-decorator';
    import './styles.scss';

    @Component
    export default class Header extends Vue {

      @Prop() private navBrand!: string;
      @Prop() private menus!: string[];

       get navHeading(): string {
            return this.navBrand;
       }

       get navMenus(): string[] {
            return this.menus;
       }
    }
</script>
