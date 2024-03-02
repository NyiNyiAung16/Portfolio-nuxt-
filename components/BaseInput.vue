<script setup>

defineProps({
    label:{
        type:String,
        default:''
    },
    modelValue:{
        type:[String,Number],
        required:true
    }
});

defineEmits(['update:modelValue'])

</script>


<template>
    <label v-if="label">{{ label }}</label>
    <input
        v-bind="$attrs"
        :value="modelValue"
        @input="$emit('update:modelValue',$event.target.value)"
    >
</template>

<style scoped>

label{
    opacity: .7;
}

input{
    min-width: 100%;
    padding: 8px;
    background-color: #fff;
    border: 1px solid #D5D5D5;
    border-radius: 5px;
    outline: none;
    box-sizing: border-box;
    box-shadow: inset 0 0 4px rgba(0,0,0,.25);
    transition: all .5s;
}

input::placeholder{
    color: rgba(0,0,0,.5);
}

input:focus{
    border-color: #7E22CE;
    box-shadow: inset 0 0 2px rgba(0,0,0,.25);
}

</style>