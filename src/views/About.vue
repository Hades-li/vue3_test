<template>
  <div class="about">
    <h1>{{ name }}</h1>
    <h3>{{title}}</h3>
    <p>{{info.age}}</p>
    <p>{{info.sex}}</p>
    <button @click="count">增加数字</button>
    <input type="text" v-model="title">
  </div>
</template>
<script>
import {ref,reactive} from 'vue'

export default {
  setup() {
    let title = '标题'
    let name = ref('小米')
    const info = reactive({
      age: 10,
      sex: '男'
    })
    const count = () => {
      info.age += 1
    }

    return {
      name,
      info,
      count,
      title
    }
  }
}
</script>
