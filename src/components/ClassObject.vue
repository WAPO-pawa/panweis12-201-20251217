<template>
    <h3>class属性绑定对象</h3>
    <div class="text" v-bind:class = "{box: isBox, border: isBorder}">
        <div v-bind:class="{inner: isInner}">春夏</div>
        <div v-bind:class="classObject">秋冬</div>
        <div v-bind:class="classMeal">三餐四季</div>
    </div>
</template>

<script>
    import {ref, reactive, compile, computed} from 'vue'
    const isBox = ref(true)
    const isBorder = ref(true)
    const isInner = ref(true)
    const isMeal = ref(true)
    const classObject = reactive({
        inner: true
    })
    const classMeal = computed(() => ({
        meal: isMeal.value}))
</script>

<style>
    .text{
        text-align: center; line-height: 30px;
    }
    .box{
        width: 100px;
        height: 10px;
        margin-bottom: 2px;
        background-color: linear-gradient(45deg, red, green);
    }
    .border{
        border: 1px solid red;
    }
    .inner{
        color: red;
    }
    .meal{
        margin-top: 2px; width: 100px; height: 10px; background-color: linear-gradient(45deg, red, green);
    }
    .meal{
        width: 100px; height: 10px; background-color: linear-gradient(45deg, red, green);
    }
</style>