<script setup>

defineProps({
    body:{
        type:String,
        required:true
    }
})

</script>


<template>
    <button 
        v-bind="$attrs"
        type="submit" 
        v-if="body"
    >
        <span>{{ body }}</span>
    </button>
</template>

<style scoped>
button{
    width: 100%;
    color: #fff;
    padding: 8px;
    border: none;
    outline: none;
    border-radius: 5px;
    background-color: #7E22CE;
    transition: all .8s;
}
button:hover,button:active{
    color: #fff;
    background-color: #6b26a8;
}

</style>
