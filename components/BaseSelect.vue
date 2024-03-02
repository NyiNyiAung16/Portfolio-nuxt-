<script setup>

defineProps({
    label:{
        type:String,
        default:''
    },
    modelValue:{
        type:Array,
        required:true
    },
    defaultName:{
        type:String,
        required:true
    },
    options:{
        type:Array,
        required:true
    }
});

defineEmits(['update:modelValue'])

</script>


<template>
    <label v-if="label">{{ label }}</label>
    <select
        v-bind="$attrs"
        :value="modelValue"
        @change="(e) => $emit('update:modelValue',Array.from(e.target.selectedOptions).map(o => o.value))"
    >
        <option selected disabled :value="modelValue">Choose a {{  defaultName }}</option>
        <option
            v-for="(option,index) in options"
            :key="index"
            :value="option"
        >
            {{ option }}
        </option>
    </select>
</template>


<style scoped>

label{
    opacity: .7;
}

select{
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

select:focus{
    border-color: #7E22CE;
    box-shadow: inset 0 0 2px rgba(0,0,0,.25);
}

select option{
    border-radius: 3px;
    padding: 3px 5px;
    margin: 5px 0;
}

</style>