<template>
  <div class="icon-wrapper">
    <component :is="name" class="icon" :size="size"></component>
    <slot></slot>
  </div>
</template>

<script>
import { UsersIcon, MapIcon } from 'vue-feather-icons'

export default {
  props: {
    size: {
      type: [Number, String],
      default: '24'
    },
    name
  },
  components: {
    UsersIcon,
    MapIcon
  }
}
</script>

<style scoped>
.icon-wrapper {
  display: inline-flex;
  align-items: center;
  color: rgba(0, 0, 0, 0.4);
  font-size: 1rem;
  font-weight: 600;
}
.icon {
  stroke: currentColor;
  stroke-width: 2;
  stroke-linecap: round;
  stroke-linejoin: round;
  fill: none;
  margin-right: 6px;
}
</style>
