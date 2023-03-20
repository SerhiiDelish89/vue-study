<template>
  <button v-on="$Listeners" v-bind:type="type" :class="{btn: true, 'btn--outlined': false}"  >
  <slot></slot>
  </button>
</template>

<script>
    export default {
    name: "HomeButton",
    props: {
      type: {
        type: String,
        default: 'button',
        required: true,
      },
      outlined: {
        type: Boolean,
        default: false
       } 
       }
    }
</script>

<style lang="scss" scoped>
.btn{
  display: inline-block;
  font-size: 18px;
  background-color: #ff662D;
  color: #fff;
  cursor: pointer;
  min-width: 220px;
  border: 1px solid transparent;
  padding: 8px 15px;


  &--outlined {
    background: none;
    border: 1px solid #FF662D;
    color: #FF662D;
  }
}
</style>