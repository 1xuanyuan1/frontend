<template>
    <form>
        <slot></slot>
    </form>
</template>
<script>
export default {
    name: 'm-form',
    provide: {
        form: this
    },
    props: {
        model: {
            type: Object,
            required: true
        },
        rules: {
            type: Object,
            default: () => ({})
        }
    }
}
</script>