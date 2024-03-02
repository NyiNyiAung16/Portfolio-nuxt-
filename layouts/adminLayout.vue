<script setup>

</script>


<template>
    <div>   
        <div class="row m-0" style="min-height: 100vh;">
            <div class="col-3 leftContainer">
                <div class="py-3">
                    <img src="/photos/1.jpg" alt="logo" class="logo">
                    <h3 class="text-center mt-2">My Portfolio</h3>   
                </div>
                <div class="line bg-white"></div>
                <div class="mt-4">
                    <NuxtLink href="/admin/dashboard" class="links">Dashboard</NuxtLink>
                    <NuxtLink href="/admin/user/profile" class="links">Profile</NuxtLink>
                    <NuxtLink href="/admin/project/create" class="links">Create Project</NuxtLink>
                </div>
            </div>
            <div class="col-9 rightContainer">
                <div class="d-flex justify-content-between align-items-center py-2">
                    <NuxtLink href="/" class="HomeLink">
                        <i class="fa-solid fa-arrow-right-from-bracket icon"></i>
                    </NuxtLink>
                    <div>
                        <p class="m-0 fs-5">NyiNyi / nyinyi@gmail.com</p>
                    </div>
                </div>
                <!-- break line -->
                <div class="line bg-secondary"></div>
                <div class="content p-3">
                    <slot/>
                </div>
            </div>
        </div>
    </div>
</template>


<style scoped>

a.router-link-active{
    border-color: #7E22CE;
    background-color: #777;
}

.logo{
    display:block;
    width: 50px;
    height: 50px;
    margin: auto;
    border-radius: 100%;
    object-fit: cover;
}

.icon{
    font-size: 23px;
    transform: rotate(180deg);
}

.leftContainer{
    background-color: #222;
    color: #fff;
    position: relative;
}
.rightContainer{
    background-color: #444;
    color: #f1f1f1;
}

.line{
    width: 100%;
    height: 2px;
    margin-top: 6px;
}

.links{
    display: block;
    margin: 7px 0;
    background-color: #8f8f8f;
    color: #f1f1f1;
    text-align: center;
    font-size: 18px;
    border-left: 5px solid transparent;
    border-radius: 3px;
    padding: 8px 15px;
    text-decoration: none;
}


.HomeLink{
    color: #f1f1f1;
    transition: all .6s;
}

.HomeLink:hover{
    color: #efefef;
    transform: translateX(-3px);
}



</style>