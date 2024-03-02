<script setup>

defineProps({
    id:{
        type:String,
        required:true
    },
    label:{
        type:String,
        default:''
    }
});


defineEmits(['change'])

</script>


<template>
    <label v-if="label" :for="id">{{ label }}</label>
    <input 
        v-bind="$attrs"
        type="file"
        class="form-control"
        :id="id" 
        @change="(e) => $emit('change',e.target.files)"
    >
</template>

<style scoped>

label{
    opacity: .7;
}
</style>
