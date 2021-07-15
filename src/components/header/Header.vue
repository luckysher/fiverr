<template src="./header.html"></template>

<script lang="ts">
    import { Component, Prop, Vue } from 'vue-property-decorator';
    import './styles.scss';

    @Component
    export default class Header extends Vue {

      @Prop() private navBrand = '';
      @Prop() private menus : string[] = [];

       // Constructor
       constructor() {
            super();

            // Nav brand
            this.navBrand = "fiverr";

            // Header navigation menus
            this.menus = ["Dashboard", "Messages", "Orders", "Gigs", "Analytics", "Earnings"];
       }
    }
</script>
