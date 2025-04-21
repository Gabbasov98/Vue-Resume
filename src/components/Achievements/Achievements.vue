<template>
    <div class="achievements m-section">
        <div class="_line"></div>
        <div class="h2">
            Achievements
        </div>

        <div class="achievements__items">
            <div
                    class="achievement-item"
                    v-for="(item, index) in achievementItems" :key="index"
            >
                <span class="achievement-item__round"></span>
                <div class="achievement-item__col">
                    <div class="achievement-item__top">
                        <div class="achievement-item__duration">
                            <div v-if="item.duration !== ''" class="text10 gray-dark-text">{{item.duration}}</div>
                            <div v-else class="achievement-item__badge">
                                <span class="text10">Present</span>
                            </div>
                        </div>
                        <div class="achievement-item__place">
                            <img src="../../assets/img/place.svg" alt="">
                            <span class="text10 gray-text">{{item.place}}</span>
                        </div>
                    </div>
                    <div class="achievement-item__bottom">
                        <div class="achievement-item__icon">
                            <img :src="$getImageUrl(item.icon)" alt="">
                        </div>
                        <div class="achievement-item__info">
                            <div class="achievement-item__prof text12 gray-text">
                                {{item.prof}}
                            </div>
                            <div class="achievement-item__name medium-text">
                                {{item.name}}
                            </div>
                        </div>
                    </div>
                </div>
                <div class="achievement-item__col2">
                    <div class="achievement-item__desc text12 gray-text">
                        {{item.desc}}
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import './Achievements.scss';
    export default {
        name: "Achievements",
        data() {
            return {
                achievementItems: [
                    {
                        icon: "company.webp",
                        place: "Chandigarh",
                        duration: "",
                        prof: "Web Developer",
                        name: "Freelance",
                        desc: "Developing web UI for e-commerce, company sites and personal sites. ",
                    },
                    {
                        icon: "company2.webp",
                        place: "Online",
                        duration: "Jun 2021 - Nov 2021",
                        prof: "Frontend developer",
                        name: "TRKR",
                        desc: "Developing frontend of Trucking app",
                    },
                ]
            }
        }
    }
</script>

<style scoped>

</style>
