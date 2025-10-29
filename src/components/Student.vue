<template>
  <div class="student">
    <h2>姓名：{{ name }}</h2>
    <h2>年龄：{{ age }}</h2>
    <h2>性别：{{ gender }}</h2>
    <button @click="changeName">修改名字</button>
    <button @click="changeAge">修改年龄</button>
    <button @click="changeGender">修改性别</button>
  </div>
</template>

<script setup name = 'Student' lang="ts">
import { ref,reactive,toRefs,toRef } from 'vue'
let student = reactive({name:'张三', age:18, gender:'男'})
let {name, age} = toRefs(student)
let gender = toRef(student, 'gender')


function changeName() {
  name.value += '~'
}


function changeAge() {
  age.value += 1
}

function changeGender() {
  gender.value = '女'
}
</script>
