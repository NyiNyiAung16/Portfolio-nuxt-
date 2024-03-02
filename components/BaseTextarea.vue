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
    <textarea 
        v-bind="$attrs"
        :value="modelValue"
        rows="4"
        @input="$emit('update:modelValue',$event.target.value)"
    >
    </textarea>
</template>

<style scoped>

label{
    opacity: .7;
}

textarea{
    min-width: 100%;
    padding: 8px;
    background-color: #fff;
    border: 1px solid #D5D5D5;
    border-radius: 5px;
    outline: none;
    box-sizing: border-box;
    box-shadow: inset 0 0 4px rgba(0,0,0,.25);
    transition: all .5s;
    resize: none;
}

textarea::placeholder{
    color: rgba(0,0,0,.5);
}

textarea:focus{
    border-color: #7E22CE;
    box-shadow: inset 0 0 2px rgba(0,0,0,.25);
}

</style>