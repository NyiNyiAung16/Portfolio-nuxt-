<script setup>

const route = useRoute();

const hideSwitchIcons = ref(true);
const defaultSwitchIcon = ref(null);

const showSwitchIcons = () => {
    hideSwitchIcons.value = !hideSwitchIcons.value;
}
const switchTheme = (name) => {
    defaultSwitchIcon.value.className = `fa-solid fa-${name}`;
    hideSwitchIcons.value = true;
    if(name === 'sun'){
        document.documentElement.style.setProperty('--whole-base-bg','#e7e7e7');
        document.documentElement.style.setProperty('--base-bg','#7e22ce');
        document.documentElement.style.setProperty('--thick-bg','#6b21a8');
        document.documentElement.style.setProperty('--animate-color','#8a3acc');
        document.documentElement.style.setProperty('--base-color','#333');
        document.documentElement.style.setProperty('--banner-icon-color','#7e22ce');
        document.documentElement.style.setProperty('--banner-icon-hover-color','#6b21a8');
    }else{    
        document.documentElement.style.setProperty('--whole-base-bg','#444');
        document.documentElement.style.setProperty('--base-bg','#000');
        document.documentElement.style.setProperty('--thick-bg','#222');
        document.documentElement.style.setProperty('--animate-color','#000');
        document.documentElement.style.setProperty('--base-color','rgba(255,255,255,.8)');
        document.documentElement.style.setProperty('--banner-icon-color','#222');
        document.documentElement.style.setProperty('--banner-icon-hover-color','#333');
        document.documentElement.style.setProperty('--wave-opacity','.8');
    }
}

let toggleClass = computed(()=>({
    'd-none' : route.path !== '/',
    'd-block' : route.path === '/'
}))

console.log(route)

</script>


<template>
    <nav class="navbar navbar-expand-md navbar-dark px-4 shadow-lg">
        <div class="navbar-brand">
            <NuxtLink href="/" class="brandTitle">My Portfolio</NuxtLink>
        </div>
        <button class="navbar-toggler" data-bs-toggle="collapse" data-bs-target="#nav">
            <i class="navbar-toggler-icon" ></i>
        </button>
        <div class="navbar-collapse collapse justify-content-end" id="nav">
            <ul class="navbar-nav">
                <li class="nav-item">
                    <NuxtLink to="/" class="nav-link">Home</NuxtLink>
                </li>
                <li class="nav-item">
                    <NuxtLink to="/projects" class="nav-link">Projects</NuxtLink>
                </li>
                <li class="nav-item" :class="toggleClass">
                    <a href="#about" class="nav-link">About</a>
                </li>
                <li class="nav-item" :class="toggleClass">
                    <a href="#skills" class="nav-link">Skills</a>
                </li>
                <li class="nav-item" :class="toggleClass">
                    <a href="#resume" class="nav-link">Resume</a>
                </li>
                <li class="nav-item" :class="toggleClass">
                    <a href="#contact" class="nav-link">Contact</a>
                </li>
                <li class="position-relative">
                    <button type="button" class="btn modeBtn" @click="showSwitchIcons">
                        <i class="fa-solid fa-sun" ref="defaultSwitchIcon"></i>
                    </button>
                    <ul class="list-group mt-1 position-absolute" :class="{'d-none':hideSwitchIcons}" style="z-index: 100;">
                        <li class="list-group-item" style="cursor: pointer;" @click="switchTheme('sun')">
                            <i class="fa-solid fa-sun"></i>
                        </li>
                        <li class="list-group-item" style="cursor: pointer;" @click="switchTheme('moon')">
                            <i class="fa-solid fa-moon"></i>
                        </li>
                    </ul>
                </li>
            </ul>
        </div>
    </nav>
</template>


<style scoped>

.brandTitle{
    color: #fff;
    text-decoration: none;
}

</style>
