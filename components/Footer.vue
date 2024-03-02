<script setup>

onMounted(()=>{
    const year = new Date().getFullYear();
    years.value.textContent = year;
})

const years = ref(null);

</script>


<template>
    <section class="footer py-3" id="contact"> <!-- bg-secondary-->
        <div class="row m-0">
            <div class="col-4">
                <div class="d-flex align-items-center gap-2">
                    <img src="/photos/myimage.jpg" alt="footerimg" width="50" class="rounded">
                    <h5 class="fw-bold text-light">NyiNyiAung</h5>
                </div>
                <p class="text-light">Lorem ipsum dolor sit amet consectetur adipisicing elit. Vero ut facere maiores ducimus saepe fugiat porro!</p>
            </div>
            <div class="col-4">
                <div class="d-inline-flex flex-column gap-2">
                    <NuxtLink to="/" class="links">Home</NuxtLink>
                    <NuxtLink to="/projects" class="links">Projects</NuxtLink>
                    <a href="#skills" class="links">Skills</a>
                    <a href="#resume" class="links">Resume</a>
                </div>
            </div>      
            <div class="col-4"> 
                <h3 class=" text-light fw-bold" style="text-decoration: underline;">Contact</h3>
                <div class="d-flex flex-column gap-2">
                    <a href="mailto:nyinyiaung200316@gmail.com" class="contactLinks">Email : nyinyiaung200316@gmail.com</a>
                    <a href="tel:09454983106" class="contactLinks">PhoneNo : 09454983106</a>
                </div>
            </div>
        </div>
        <p class="text-center copyright m-0 mt-3">Copy Right &copy; <span ref="years"></span> by NyiNyiAung</p>
    </section>
</template>

