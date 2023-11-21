<template>
    <div class="projectMainDiv" id="project">
        <div class="projectDiv">
            <div class="apporachingDiv">
                <h1>GLIMPSE OF MY PROJECT.</h1>
                <lord-icon id="icon" src="https://cdn.lordicon.com/uqpazftn.json" trigger="loop" delay="1000"
                    colors="primary:#000000,secondary:#9c9c9c" style="width:128px;height:128px">
                </lord-icon>
                <h3>I successfully led a multifaceted project encompassing website, mobile app creation and desktop.
                    Combining my technical expertise and creativity,
                    I delivered a comprehensive digital solution tailored to client needs.</h3>
            </div>
            <div class="projectImageDiv">
                <div v-for="project in projects">
                    {{project.title}}
                    <img class="projectImage" :src="`/src/assets/Images/${project.image}`" :alt="project.image">
                </div>
            </div>
        </div>
        
    </div>
</template>

<script>

    export default{
        props:{
            projects : Object
        },
    }
    

</script>
<style>
.projectDiv {
    padding-block: min(3vw, 2rem);
    padding-inline: min(10vw, 20rem);
    display: flex;
    gap: 3vw;
}

.projectImageDiv {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    place-content: center;
    gap: 2vw;
}

.apporachingDiv {
    text-align: center;
    display: grid;
    place-content: center;
}

.apporachingDiv h1 {
    font-size: calc(3vw + 1.5rem);
    margin: 0px;
}

.apporachingDiv h3 {
    font-size: calc(1vw + .2rem);
    color: #9c9c9c;
}

#icon {
    transform: translate(-50%);
    margin-left: 50%;
}

.projectImage {
    height: calc(20vw + 3rem);
    width: calc(25vw + 3rem);
}

@media (width <=768px) {
    .projectDiv {
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    .projectImage {
        width: 100%;
    }
}

@media (width <=428px) {
    .projectImageDiv {
        grid-template-columns: repeat(1, 1fr);
        place-content: center;
        place-items: center;
    }

    .projectImageDiv div {
        width: 70%;
    }
}
</style>