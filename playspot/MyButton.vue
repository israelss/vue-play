<template>
  <button class="button" :style="{color: color, borderColor: color}" @click="handleClick" :class="{rounded: rounded}"><slot></slot></button>
</template>

<script>
  export default {
    props: {
      rounded: Boolean,
      handleClick: {
        default: () => () => null
      },
      color: {
        default: '#42b983'
      }
    }
  }
</script>

<style>
  .button {
    border: 2px solid;
    padding: 10px 20px;
    border-radius: 3px;
    background-color: white;
    outline: none;
  }
</style>
