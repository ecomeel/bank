<template>
  <header :class="$style.header">
    <div :class="$style.header__menu">
      <div v-for="index in 3" :key="index" />
    </div>
    <h1 :class="$style.header__title">{{ $route.name }}</h1>
    <div :class="$style['header__right-content']">
      <ButtonImageCircle 
        :class="$style.header__avatar"
      />
      <ButtonImageCircle 
        button-name="Уведомления"
        image-url="/images/icons/notification.svg"
      />
      <ButtonImageCircle 
        button-name="Настройки"
        image-url="/images/icons/settings.svg"
      />
    </div>
  </header>
</template>
  
<script setup lang='ts'>
import ButtonImageCircle from '@/components/buttons/ButtonImageCircle.vue'
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
  &__right-content {
    display: flex;
    flex-direction: row-reverse;
    align-items: center;
    gap: 25px;
  }
  
  @media (min-width: $screen-m-min) {
    &__menu {
      display: none;
    }
    &__title {
      font-size: 25px;
    }
    &__avatar {
      width: 40px;
      height: 40px;
    }
  }
  @media (min-width: $screen-xl-min) {
    padding: 1.2vw 2.78vw;
    &__title {
      font-size: 1.94vw;
    }
    &__avatar {
      width: 3.47vw;
      height: 3.47vw;
    }
  }
}
</style>