<template lang="html">
    <RadSideDrawer ref="drawer" drawerLocation="Left" gesturesEnabled="true" :drawerTransition="transition">
        <StackLayout ~drawerContent backgroundColor="#ffffff">
            <slot name="drawerContent"/>
        </StackLayout>
        <Frame ~mainContent ref="drawerMainContent">
            <slot name="mainContent"/>
        </Frame>
    </RadSideDrawer>
</template>

<script lang="ts">
  import Vue from "vue";
  import {SlideInOnTopTransition} from 'nativescript-ui-sidedrawer';

  export default Vue.extend({
    data() {
      return {
        transition: new SlideInOnTopTransition()
      }
    }
  });
</script>

<style scoped lang="scss">
    // Start custom common variables
    @import '~@nativescript/theme/scss/variables/blue';
    // End custom common variables

    // Custom styles
</style>
