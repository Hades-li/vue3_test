<template>
  <transition name="el-zoom-in-top">
    <div v-show="visible">
      <span>消失</span>
      <button @click="sw">
        点击
      </button>
    </div>
  </transition>
</template>

<script>
  import {ref, onUpdated, getCurrentInstance} from 'vue'

  export default {
    name: 'Test',
    setup(props, ctx) {
      const visible = ref(true)
      function sw() {
        visible.value = !visible.value
      }
      onUpdated(() => {
        console.log(visible.value)
      })
      return {
        visible,
        sw
      }
    }
  }
</script>

<style scoped>

</style>
