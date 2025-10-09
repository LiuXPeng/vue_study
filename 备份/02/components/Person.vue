<template>
<div class="person">
    <h2>{{ name }}</h2>
    <h2>年龄：{{ age  }}</h2>
    <button @click="changeName">修改名字</button>
    <button @click="changeAge">修改年龄</button>
    <button @click="showTel">查看联系方式</button>
</div>
</template>

<script lang="ts">
export default {
    name: 'Person',
    data(){
        return {
            name: '李一丹',
            age:18,
            tel:'1212121'
        }
    },
    methods:{
        changeName(){
            this.name = 'lisi'
        },
        changeAge(){
            this.age+=1
        },
        showTel(){
            alert(this.tel)
        }
    }
}
</script>

<style scoped></style>