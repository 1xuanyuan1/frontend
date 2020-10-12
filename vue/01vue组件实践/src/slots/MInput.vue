<template>
    <div>
        <input v-bind="$attrs" @input="onInput"/>
    </div>
</template>
<script>
export default {
    name: 'm-input',
    inject: ['form'],
    created() {
        console.log(this)
    },
    methods: {
        onInput(e) {
            console.log(e, e.target)
            this.$emit('input', e.target.value)
        }
    },
}
</script>