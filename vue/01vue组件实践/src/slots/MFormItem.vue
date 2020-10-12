<template>
    <div>
        <label v-if="label">{{label}}</label>
        <slot></slot>
        <p v-if="error">{{error}}</p>  
    </div>
</template>
<script>
import Schema from 'async-validator';
export default {
    name: 'm-form-item',
    props: {
        label: {
            type: String,
            default: ''
        }
    },
    data() {
        return {
            error: ''
        }
    },
    created() {
        console.log(Schema)
    },
    methods: {
        validate () {
            
        }
    },
}
</script>