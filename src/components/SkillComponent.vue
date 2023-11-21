<template>
    <div class="skillMainDiv">
        <div class="heading">
            <h1>Service, I provide!</h1>
            <hr>
        </div>
        <div class="what-I-offer">
            <div class="serviceDiv">
                <div class="service" id="service-one" v-for="service in services">
                    <div class="serviceHeading">
                        <h3>{{service.title}}</h3>
                        <lord-icon :src="`https://cdn.lordicon.com/${this.arrow}.json`" trigger="hover"
                            colors="primary:#000000" style="width:32px;height:32px">
                        </lord-icon>
                    </div>
                    <div class="serviceContent" :id="service.id">
                        {{service.content}}
                    </div>
                </div>
            </div>
            <div class="skill">
                <div class="skillsDiv">
                    <div class="skill" v-for="skill in skills">
                        <img :src="`src/assets/Images/${skill.image}`" :alt="skill.title" :title="skill.title" id="skill">
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>


<script>
export default {
    data() {
        return {
            arrow: "rxufjlal",
            services: [
                {
                    'title': 'Website Design and Development', 'id': 'serviceContentOne',
                    'content': 'Passionate web designer & developer creating stunning, user-friendly websites to elevate brands and enhance online experiences.'
                },
                {
                    'title': 'Mobile Application', 'id': 'serviceContentTwo',
                    'content': 'Experienced in mobile app development, creating user-friendly, innovative, and scalable solutions for various platforms.'
                },
                {
                    'title': 'Desktop Application', 'id': 'serviceContentThree',
                    'content': 'Crafting efficient, user-friendly desktop apps that elevate user experiences and solve real-world problems with precision.'
                },
            ]
        }
    },
    props: {
        skills: Object
    },
}
</script>

<style scoped>
.skillMainDiv {
    padding-top: min(5vw, 3rem);
    padding-inline: min(10vw, 20rem);
}

.what-I-offer {
    margin-block: 5vw;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 3vw;
}

.service {
    border-bottom: 1px solid rgba(167, 167, 167, 0.486);
    padding-block: 1vw;
}

.service .serviceHeading {
    display: flex;
    gap: 1vw;
    align-items: center;
}
.service .serviceHeading h3 {
    margin: 0px;
}

.service .serviceContent {
    overflow: hidden;
    text-align: justify;
    min-height: 0vw;
    color: #9c9c9c;
}

.heading h1 {
    font-size: calc(3vw + 1.5rem);
    text-align: center;
    padding: 0;
    margin-bottom: 0;
}

.heading hr {
    width: 25vw;
    height: 4px;
    background: #9c9c9c;
    border-radius: 8px;
    border: none;
}

.skillsDiv {
    padding-block: min(5vw, 3rem);
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    place-content: center;
    place-items: center;
    gap: 7vw;
}

#skill {
    height: 64px;
    width: 64px;
}

#skill:hover {
    transform: scale(1.1);
    filter: drop-shadow(3px 20px 4px rgba(0, 0, 0, 0.747));
}

@media (width <=768px) {
    .what-I-offer {
        flex-direction: column;
    }
}

@media (width <=425px) {
    .skillsDiv {
        grid-template-columns: repeat(3, 1fr);
        gap: 15vw;
    }
}
</style>