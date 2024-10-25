<template>
  <header :class="$style.header">
    <div :class="$style.header__menu">
      <div v-for="index in 3" :key="index" />
    </div>
    <h1 :class="$style.header__title">{{ $route.name }}</h1>
    <div :class="$style['header__right-content']">
      <div :class="$style.header__avatar">
        <!-- TODO: insert avatar -->
        <!-- <img src="" alt=""> -->
      </div>
      <!-- TODO: add settings -->
       <!-- TODO: add notifs -->
        <!-- TODO: Add search something -->
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
    width: 18px;
    height: 14px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    cursor: pointer;

    & > div {
      height: 2px;
      width: 100%;
      background-color: $dark-blue;
      border-radius: 10px;
    } 
  }
  &__title {
    font-size: 20px;
    font-weight: 600;
    text-transform: capitalize;
  }
  &__avatar {
    width: 35px;
    height: 35px;
    border-radius: 100%;
    background-color: $gray-b1b;
    cursor: pointer;
  }
}
</style>