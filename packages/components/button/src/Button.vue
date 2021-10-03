<template>
  <button class="c-button" v-bind="$attrs" v-on="$listeners">
    <slot />
  </button>
</template>

<script lang="ts">
import { Vue, Component } from 'vue-property-decorator'

@Component({
  inheritAttrs: false,
})
export default class CButton extends Vue {}
</script>

<!--<style>-->
<!--.c-button {-->
<!--  background: #000-->
<!--}-->
<!--</style>-->
