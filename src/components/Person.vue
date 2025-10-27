<template>
  <div class="person">
    <h2>姓名：{{ name }}</h2>
    <h2>年龄：{{ age }}</h2>
    <button @click="changeName">修改名字</button>
    <button @click="changeAge">修改年龄</button>
    <button @click="showTel">查看联系方式</button>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'
let name = ref('张三')
let age = ref(18)
let tel = '12323231231'


function changeName() {
  name.value = 'lisi'
}


function changeAge() {
  age.value += 1
}

function showTel() {
  alert(tel)
}
</script>
