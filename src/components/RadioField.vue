<template>
  <div class="q-pa-md">
    <div class="text-subtitle1">问题 {{no}} ：{{ title }}</div>
    <q-option-group
      v-model="result"
      :options="content"
      color="primary"
      :inline="inline"
    />
    <div v-if="result != null" class="text-subtitle2">你的选择是：{{ radioSelect }}</div>
  </div>
</template>

<script>
export default {
  name: 'RadioField',
  props: ['title', 'no', 'content', 'inline'],
  data () {
    return {
      result: null
    }
  },
  computed: {
    radioSelect: function () {
      return this.result
    }
  }
}
</script>

<style scoped>

</style>
