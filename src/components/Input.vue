<template>
    <input type="text" :value="modelValue" @input="$emit('update:modelValue', $event.target.value)">
</template>

<script>
export default {
    name: 'Input',
    props: {
        modelValue: String
    }
}
</script>

<style scoped>
input[type='text'] {
    text-align: center;
    display: block;
    width: 250px;
    padding: 6px 12px;
    font-size: 14px;
    line-height: 1.4;
    color: #555;
    background-color: #fff;
    background-image: none;
    border: 1px solid #ccc;
    border-radius: 4px;
}
</style>