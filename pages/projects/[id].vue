<script setup>

definePageMeta({
    layout:'projects-layout'
});

const route = useRoute();

const project = ref({});

onMounted(async()=>{
    const data = await fetch('/projects.json'); 
    const parseData = await data.json();
    project.value = parseData.projects.find((p)=>{
        return p.id === parseInt(route.params.id);
    });
});


</script>

<template>
    <Head>
        <Title>My Portfolio | Detail</Title>
    </Head>
    <div class="detailContainer container mt-5" v-if="project">  
        <div class="row">
            <div class="col-10 px-3 mx-auto">
                <Carousel
                    :default-photo="project.photo"
                    :photos="project.photos"
                />
                <div class="mt-3 detailTexts">
                    <h3 class="fw-bold fs-3 m-0">{{ project.title }}</h3>
                    <p class="m-0 mb-1 mt-2" style="font-size: 18px;">{{ project.description }}</p>
                </div>
                <div class="d-flex gap-3 align-items-center mt-4">
                    <p 
                        class="px-2 py-1 rounded bg-secondary text-light" 
                        v-for="(skill,index) in project.skills" 
                        :key="index" 
                        style="user-select: none;"
                    >
                        {{ skill }}
                    </p>
                </div>
            </div>
        </div> 
    </div>
</template>

<style scoped>

.image{
    max-width: inherit;
    max-height: 340px;
    height: 100%;
    object-fit: cover;
}

</style>