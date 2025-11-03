<template>
  <div class="person">
    <h2>姓名：{{ name }}</h2>
    <h2>年龄：{{ age }}</h2>
    <button @click="changeName">修改名字</button>
    <button @click="changeAge">修改年龄</button>
    <button @click="showTel">查看联系方式</button>


    <h2>姓：<input type="text" v-model="firstName"></input></h2>
    <h2>名：<input type="text" v-model="secondName"></input></h2>
    <h2>全名：{{ fullName }}</h2>
    <button @click="changeFullName">全名改为：li-si</button>
  </div>
</template>

<script setup lang="ts">
import { ref, computed } from 'vue'
let name = ref('张三')
let age = ref(18)
let tel = '12323231231'

let firstName = ref('张')
let secondName = ref('三')

// let fullName = computed(()=>{
//     return firstName.value + '-' + secondName.value
//  })

let fullName = computed({
  get() {
    return firstName.value + '-' + secondName.value
  },

  set(val) {
    console.log('有人修改了fullName', val)
    firstName.value = val.split('-')[0]
    secondName.value = val.split('-')[1]
  }
})

function changeFullName() {
  fullName.value = 'li-si'
}


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
