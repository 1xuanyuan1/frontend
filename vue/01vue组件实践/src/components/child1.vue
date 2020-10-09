<template>
    <div>
        <h2>子组件1</h2>
        <p>{{$attrs.msg}}</p>
        <button @click="eat">吃饭</button>
        <button @click="eat2">叫弟弟吃饭</button>
    </div>
</template>
<script>
export default {
    name: 'child1',
    methods: {
        eat () {
            console.log('儿子1吃饭')
        },
        eat2 () {
            this.$parent.$emit('eat')
        }
    },
}
</script>