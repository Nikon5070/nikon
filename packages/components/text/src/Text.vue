<template>
  <component :is="tag" class="c-text" v-bind="$attrs" v-on="$listeners">
    <slot />
  </component>
</template>

<script lang="ts">
import { Vue, Component, Prop } from 'vue-property-decorator'

@Component({
  inheritAttrs: false,
})
export default class CText extends Vue {
  @Prop({
    type: String,
    default: 'span'
  })
  readonly tag!: string
}
</script>

<style lang="stylus" scoped>
.c-text
  background red
</style>
