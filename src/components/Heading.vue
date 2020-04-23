<template>
  <component :is="as">
    <slot />
  </component>
</template>

<script>
export default {
  props: {
    as: String,
  },
}
</script>
