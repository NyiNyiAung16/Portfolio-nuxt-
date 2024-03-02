<script setup>

defineProps({
    defaultPhoto:{
        type:String,
        default:''
    },
    photos:{
        type:Array,
        default:[]
    }
});

</script>


<template>
    <div class="carousel slide" data-bs-ride="true" id="carouselSection" v-if="defaultPhoto">
        <div class="carousel-inner">
            <div class="carousel-item active">
                <img :src="defaultPhoto" class="d-block rounded" alt="carouselPhoto">
            </div>
            <div class="carousel-item" v-for="(photo,index) in photos" :key="index">
                <img :src="photo" class="d-block rounded" alt="carouselPhoto">
            </div>
        </div>
        <button class="carousel-control-prev" type="button" data-bs-target="#carouselSection" data-bs-slide="prev">
            <span class="carousel-control-prev-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Previous</span>
        </button>
        <button class="carousel-control-next" type="button" data-bs-target="#carouselSection" data-bs-slide="next">
            <span class="carousel-control-next-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Next</span>
        </button>
    </div>
</template>


<style scoped>
.carousel .carousel-inner .carousel-item img{
    width: 100%;
    max-height: 450px;
    height: 100%;
    object-fit: cover;
}

</style>

