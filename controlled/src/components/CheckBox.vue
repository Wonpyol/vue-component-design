<template>
  <input type="checkbox" :value="value" @click="this.$emit('input', !value)">
</template>

<script>
export default {
  name: "CheckBox",
  //부모에게는 'input' 이벤트
  //자식은 value props로 받음
  props: ['value']
}
</script>

<style scoped>

</style>