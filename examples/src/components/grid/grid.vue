<template>
  <div class="i-grid" v-bind:class="iClass">
    <slot></slot>
  </div>
</template>

<script>
export default {
  props: {
    iClass: {
      type: String,
      default: ''
    }
  }
}
</script>

