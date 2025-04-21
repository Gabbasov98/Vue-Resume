<template>
    <div class="education m-section">
        <div class="_line"></div>
        <div class="h2">
            Education
        </div>

        <div class="education__items">
            <div
                    class="education-item"
                    v-for="(item, index) in educationItems" :key="index"
            >
                <div class="education-item__top">
                    <div class="education-item__icon">
                        <img :src="$getImageUrl(item.icon)" alt="">
                    </div>
                    <div class="education-item__name text12 medium-text">
                        {{item.name}}
                    </div>
                </div>
                <div class="education-item__title text14 medium-text">
                    {{item.title}}
                </div>
                <div class="education-item__date text10 gray-text">
                    {{item.date}}
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import './Education.scss';
    export default {
        name: "Education",
        data() {
            return {
                educationItems: [
                    {
                        icon: "univer.webp",
                        name: "Guizhou Normal University",
                        title: "Master in Management Science",
                        date: "2019 - 2021",
                    },
                    {
                        icon: "univer.jpg",
                        name: "Kazan University",
                        title: "Bachelor in Economics",
                        date: "2015 - 2019",
                    },
                ]
            }
        }
    }
</script>

<style scoped>

</style>
