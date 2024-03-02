<script setup>

function download(e){
    location.href = '/cv/NyiNyi.pdf';
}


</script>

<template>
    <section class="resumeSection py-3" id="resume" ref="resumeSection">
        <h2 class="text-center">Resume</h2>
        <div class="container row m-0 mx-auto mt-3">
            <div class="col-lg-4 mb-3 resumeleft">
                <div class="d-flex flex-column align-items-center justify-content-center">
                    <img src="/photos/3.jpg" alt="resumeimg" class="resumeImg">
                    <div class="mt-3">
                        <h3>FullStack Junior <br/> Web Developer</h3>
                    </div>
                </div>
            <button class="resumeDown" data-bs-toggle="modal" data-bs-target="#resumeModal" id="resumeDownloadTag" >
                    <span></span>
                    <span></span>
                    <span></span>
                    <span></span>
                    <span></span>
                    Get Resume
            </button>
            </div>
            <div class="col-lg-8">
                <div class="personalInformation mb-5" >
                    <h3><i class="fas fa-map-marker-alt"></i> Personal Information</h3>
                    <div class="ms-4">
                        <p>Email: nyinyiaung200316@gmail.com</p>
                        <p>Phone: 09454983106</p>
                        <p> Address: Yangon,Hmawbi</p>
                    </div>
                </div>

                <div class="personalsum mb-5">
                    <h3><i class="fas fa-map-marker-alt"></i> Personal Summary</h3>
                    <div class="ms-4">
                        <p>
                            I have been learning programming for 1year by my-self and classes. In these one year, I did a lot of projects on my own for improving my programming skills and debugging skill. I want to be a software enginner in the future and want to create like facebook and twitter. To be a software engineer, I always keep learing new things and doing projects to make things better with the knowledge i already know. I also love coding and it gives me pleasure. 
                        </p>
                    </div>
                </div>

                <div class="education mb-5">
                    <h3><i class="fas fa-map-marker-alt"></i> Education</h3>
                    <div class="ms-4">
                        <p>I have finished high school in 2019.I also finished Diploma in Network Communication in KMD Institute. I finished N4 level in Japanese and My english skill is also reached in pre-intermediate level.</p>
                    </div>
                </div>

                <div class="experience">
                    <h3><i class="fas fa-map-marker-alt"></i> Work Experience</h3>
                    <div class="ms-4">
                        <p>I have no experience in work but I am always doing my own projects and posted in github.  That’s why I have a little experience in projects. You can see my projects on my github.</p>
                    </div>
                </div>
            </div>
        </div>

        <!-- modal section -->
        <div class="modal" id="resumeModal">
            <div class="modal-dialog modal-dialog-centered">
                <div class="modal-content">
                    <div class="modal-header d-flex align-items-center">
                        <h4 class="p-0 m-0 text-dark fw-700">Are you sure to download?</h4>
                        <button class="btn-close" data-bs-dismiss="modal"></button>
                    </div>
                    <div class="modal-footer d-flex justify-content-center">
                        <button class="btn px-5 py-2 btn-warning"  data-bs-dismiss="modal" @click="download(event)">Yes</button>
                        <button class="btn px-5 py-2 btn-danger" data-bs-dismiss="modal">NO</button>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>
