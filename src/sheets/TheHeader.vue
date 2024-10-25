<template>
  <header :class="$style.header">
    <div :class="$style.header__menu">
      <div />
      <div />
      <div />
    </div>
    <h1 :class="$style.header__title">Current page</h1>
    <div :class="$style['header__right-content']">
      <div>Profile</div>
    </div>
  </header>
</template>
  
<script setup lang='ts'>

</script>
  
<style lang="scss" module>
.header {
  padding: 25px 25px 20px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: $white;

  &__menu {

  }
}
</style>