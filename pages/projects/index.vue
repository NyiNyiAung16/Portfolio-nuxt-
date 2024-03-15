<script setup>

definePageMeta({
    layout:'projects-layout'
});

const projects = ref([]);

onMounted(async()=>{
    const data = await fetch('/projects.json'); 
    const parseData = await data.json();
    projects.value = parseData.projects;
});

</script>

<template>
    <Head>
        <Title>My Portfolio | Projects</Title>
    </Head>
    <div class="container-fluid mt-5">   
        <div class="row justify-content-center">
            <div 
                class="col-3"
                v-for="project in projects" :key="project.id"
                style="min-width: 400px;"
            >
                <div class="card mb-3">
                    <img :src="project.photo" :alt="project.alt" class="card-img-top image">
                    <div class="card-content mt-2 p-2">
                        <h5 class="card-title m-0 mb-2" style="font-weight: 550;">{{ project.title }}</h5>
                        <p class="card-text m-0 mb-1" style="font-size:15px;">{{ project.description.substring(0,70) + '...' }}</p>
                    </div>
                    <NuxtLink :to="`/projects/${project.id}`" class="btn mx-2 my-1 cardButtons">Details</NuxtLink>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.image{
    max-height: 270px;
    object-fit: cover;
}

</style>