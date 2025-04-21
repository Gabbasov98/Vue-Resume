<template>
    <div class="skills m-section">
        <div class="_line"></div>
        <div class="h2">
            Tools/Skills
        </div>

        <div class="skills__items">
            <div
                    class="skill-item"
                    v-for="(item, index) in skillItems" :key="index"
            >
                <div class="skill-item__icon">
                    <img :src="$getImageUrl(item.icon)" alt="">
                </div>
                <div class="skill-item__title text14 medium-text">
                    {{item.title}}
                </div>
                <div class="skill-item__desc text10 gray-text">
                    {{item.desc}}
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import './Skills.scss';
    export default {
        name: "Skills",
        data() {
            return {
                skillItems: [
                    {
                        icon: "HTML.png",
                        title: "HTML 5",
                        desc: "Structural Design",
                    },
                    {
                        icon: "CSS.png",
                        title: "CSS 3",
                        desc: "Style Design",
                    },
                    {
                        icon: "Javascript.png",
                        title: "Javascript",
                        desc: "Web development",
                    },
                    {
                        icon: "Vue.png",
                        title: "Vue",
                        desc: "Web development",
                    },
                    {
                        icon: "React.png",
                        title: "React",
                        desc: "Web development",
                    },
                    {
                        icon: "Wordpress.png",
                        title: "Wordpress",
                        desc: "Web development",
                    },
                ]
            }
        }
    }
</script>

<style scoped>

</style>
