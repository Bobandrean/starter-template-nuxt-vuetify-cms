<template>
  <v-card
    v-bind="$attrs"
    :loading="loading"
    class="pa-15"
    :width="width"
    max-width="1000"
  >
    <slot></slot>
  </v-card>
</template>
<script>
export default {
  name: 'BaseCard',
  props: {
    width: {
      type: [String, Number],
      default: '100%',
    },
    elevation: {
      type: Number,
      default: 1,
    },
  },
  data() {
    return {
      loading: false,
      selection: [],
    }
  },
}
</script>
<style lang="scss" scoped>
.v-sheet.v-card {
  border-radius: 20px !important;
}
</style>
