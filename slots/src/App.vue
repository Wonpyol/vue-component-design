<template>
  <div>
    <ul>
      <item>아이템1</item>
      <item>
        <small>아이템2</small>
      </item>
      <item>
        <small>아이템3</small>
        <button>버튼</button>
      </item>
    </ul>

  </div>
</template>
<script>
import item from "@/components/Item.vue";
export default {
  components:{
    item
  },
}
</script>

<style scoped>
</style>
