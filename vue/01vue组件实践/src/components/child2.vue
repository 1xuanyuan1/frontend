<template>
    <div>
        <h2 v-on="$listeners">子组件2</h2>
        <p>{{foo}} - {{color}}</p>
    </div>
</template>
<script>
export default {
    name: 'child1',
    inject: {
        color: {from: 'color'}
    },
    props: {
        foo: {
            type: String,
            default: ''
        }
    },
    created() {
        this.$parent.$on('eat', () => {
            console.log('儿子2吃饭')
        })
    },
}
</script>