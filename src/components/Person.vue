<template>
<div class="person">
    <h2>姓名：{{ name }}</h2>
    <h2>年龄：{{ age  }}</h2>
    <button @click="changeName">修改名字</button>
    <button @click="changeAge">修改年龄</button>
    <button @click="showTel">查看联系方式</button>
</div>
</template>

<script lang="ts">
export default {
    name: 'Person',
    setup(){
        let name = 'zhangsan'
        let age = 18
        let tel = 12232312

        function changeName(){
            name = 'lisi'
        }

        function changeAge(){
            age+=1
        }

        function showTel(){
            alert(tel)
        }

        return {name, age, changeName, changeAge, showTel}

        // return function(){
        //     return "haha"
        // }
    }
}
</script>

<style scoped></style>