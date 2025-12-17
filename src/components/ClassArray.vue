<template>
    <h3 style="color:red;">class属性绑定数组</h3>
    <div v-bind:class = "[activeClass, borderClass]">
        梦想
    </div>
    <div v-bind:class = "[isActive? activeClass:borerClass]">
        实现
    </div>
    <div v-bind:class = "[{active: isActive}, borderClass]">
        未来
    </div>

    
</template>

<script setup>
    import { ref } from 'vue'
    const isActive = ref(true)
    const activeClass = ref('active')
    const borerClass = ref('border')

</script>

<style>
    .active{
        color: red;
        width: 100px;
        height: 10px;
        margin-bottom: 2px;
        background-color: green;
    }
    .border{
        border: 1px solid red;
    }
</style>