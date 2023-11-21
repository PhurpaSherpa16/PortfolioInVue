<script>
import NavBarComponents from '../components/NavBarComponents.vue';
import ProjectsComponents from '../components/ProjectsComponents.vue';
import IndexPageComponents from '../components/IndexPageComponents.vue';
import SecondPageComponents from '../components/SecondPageComponent.vue';
import SkillComponents from '../components/SkillComponent.vue';
import AboutAndContactComponents from '../components/AboutAndContactComponent.vue';

export default {
    components: {
        NavBarComponents,
        IndexPageComponents,
        SecondPageComponents,
        ProjectsComponents,
        SkillComponents,
        AboutAndContactComponents,
    },
    data() {
        return {
            projects: [{ "id": 1, "image": "one.jpg", "title": "Portfolio" },
            { "id": 2, "image": "two.jpeg", "title": "E-Commerce Web-Application" },
            { "id": 3, "image": "three.jpg", "title": "Mobile Design and Development" },
            { "id": 4, "image": "four.jpg", "title": "Desktop Application" }],


            skills: [{ "image": "html.png", "title": "HTML" },
            { "image": "css.png", "title": "CSS" },
            { "image": "python.png", "title": "Python" },
            { "image": "js.png", "title": "JS" },
            { "image": "android.png", "title": "Android" },
            { "image": "figma.png", "title": "Figma" },
            ],

        }
    },
}
</script>

<template>
    <div class="mainDiv">
        <div class="navDiv">
            <NavBarComponents />
        </div>
        <div>
            <IndexPageComponents />
        </div>
        <div>
            <SecondPageComponents />
        </div>
        <div>
            <ProjectsComponents :projects="projects" />
        </div>
        <div>
            <SkillComponents :skills="skills" />
        </div>
        <div>
            <AboutAndContactComponents />
        </div>
    </div>
</template>

<style scoped>
.mainDiv {
    overflow: hidden;
}

.navDiv {
    position: fixed;
    width: 100vw;
    z-index: 100;
    background: white;
    box-shadow: 1px 1px 20px rgba(129, 129, 129, 0.466);
}
</style>

