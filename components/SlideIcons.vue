<script setup>

</script>


<template>
    <div class="playIconsMain py-3" style="overflow: hidden;">
        <div class="running">
            <div class="d-flex align-items-center justify-content-center">
                <i class="fab fa-vuejs VueJs"></i>
                <i class="fab fa-laravel Laravel"></i>
                <i class="fab fa-html5 html5"></i>
                <i class="fab fa-css3-alt css3"></i>
                <i class="fab fa-js Javascript"></i>
                <i class="fab fa-bootstrap bootstrap"></i>
                <i class="fab fa-font-awesome fontawesome"></i>
                <img src="/photos/tailwind-css-icon.png" width="62">
            </div>
        </div>
    </div>
</template>

<style scoped>
.running{
    display: inline-block;
    overflow: hidden;
    animation: run 20s linear infinite;
}

@keyframes run {
    0%{
        transform: translateX(-100%);
    }
    75%{
        transform: translateX(100%);
    }
    100%{
        transform: translateX(150%);
    }
}

</style>