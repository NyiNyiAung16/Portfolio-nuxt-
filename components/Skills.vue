<script setup>

// const skillSection = ref(null);

// onMounted(()=>{
//     window.addEventListener('scroll',()=>{
//         if(window.scrollY > 60) {
//             skillSection.value.classList.add('skillsAnimation')
//         }
//     })
// })

</script>


<template>
    <div class="skillSection py-4" id="skills" ref="skillSection">
        <div>
            <h2 class="text-center fs-1 skillCaption">Skills</h2>
            <div class="container row justify-content-center gap-3 mx-auto iconContainer">
                <div class="col-lg-5 d-flex skillIcon">
                    <div class="icon">
                        <i class="fab fa-laravel Laravel"></i>
                        <span>Laravel</span>
                    </div>
                    <div class="icon">
                        <i class="fab fa-vuejs VueJs"></i>
                        <span>VueJs</span>
                    </div>
                    <div class="icon">
                        <i class="fab fa-js Javascript"></i>
                        <span>Javascript</span>
                    </div>
                    <div class="icon">
                        <i class="fab fa-html5 html5"></i>
                        <span>HTML5</span>
                    </div>
                </div>
                <div class="col-lg-5 d-flex gap- skillIcon">
                    <div class="icon">
                        <i class="fab fa-css3-alt css3"></i>
                        <span>CSS3</span>
                    </div>
                    <div class="icon">
                        <i class="fab fa-font-awesome fontawesome"></i>
                        <span>Fontawesome Icon</span>
                    </div>
                    <div class="icon">
                        <i class="fab fa-bootstrap bootstrap"></i>
                        <span>Bootstrap</span>
                    </div>
                    <div class="icon">
                        <img src="/photos/tailwind-css-icon.png" width="80" class="mx-auto mb-2">
                        <span>TailwindCss</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>

.skillsAnimation{
    animation: ani .8s ease-in;
}

@keyframes ani {
    0%{
        opacity: 0;
        transform: translateY(60px);
    }
    50%{
        opacity: 0.5;
        transform: translateY(30px);
    }
    75%{
        opacity: 0.6;
        transform: translateY(10px);
    }
    100%{
        opacity: 1;
        transform: translateY(0px);
    }
}

</style>
