<template>
  <div :class="$style.button">
    <slot>
      <img v-if="imageUrl"
        :alt="buttonName"
        :src="imageUrl"
      >
    </slot>
  </div>
</template>
  
<script setup lang='ts'>
import type { ColorNames } from '@/types/common'
import { colorGetter } from '@/constants/colors'

interface IButton {
  backgroundColor?: ColorNames;
  imageUrl?: string;
  buttonName?: string
  borderRadius?: string;
  isActive?: boolean
}

const props = withDefaults(defineProps<IButton>(), {
  backgroundColor: 'grayF5F',
  imageUrl: '',
  buttonName: 'Icon',
  borderRadius: '100%',
  isActive: false
})

const backgroundColor = colorGetter[props.backgroundColor]
</script>
  
<style lang="scss" module>
.button {
  padding: 11px;
  background-color: v-bind('backgroundColor');
  border-radius: v-bind('$props.borderRadius');
  // @if (v-bind('$props.isActive')) {
  //   cursor: pointer;
  // }
  img {
    width: 18px;
    height: auto;
  }
  @media (min-width: $screen-m-min) {

  }
  @media (min-width: $screen-xl-min) {
    padding: .9vw;
    img {
      width: 1.74vw;
    }
  }
}
</style>