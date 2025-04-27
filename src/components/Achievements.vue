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
                            <img src="../assets/img/place.svg" alt="">
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

<style lang="scss">
    .achievements{
        &__items{
            margin-top: 2em;
        }
    }

    .achievement-item{
        padding-left: 2.5em;
        padding-bottom: 1.25em;
        padding-top: .375em;
        position: relative;
        display: grid;
        grid-template-columns: 15.125em calc(100% - 15.625em);
        gap: .5em;
        &:after{
            content: '';
            position: absolute;
            top: 1.5em;
            left: .75em;
            transform: translateX(-50%);
            width: 1px;
            height: calc(100% - 1.5em);
            background-color: $gray-light2;
        }
        &__round{
            position: absolute;
            top: 0;
            left: 0;
            width: 1.5em;
            height: 1.5em;
            @include bgImgSize(100%);
            &:before{
                content: '';
                @include centerAbsolute;
                background-color: #2E2E48;
                border-radius: 50%;
                width: .375em;
                height: .375em;
            }
        }
        &__top{
            display: flex;
            align-items: center;
        }
        &__place{
            display: flex;
            align-items: center;
            margin-left: .25em;
            img{
                margin-right: .25em;
                width: .75em;
            }
        }
        &__badge{
            display: flex;
            align-items: center;
            padding: 0 .2em;
            height: 1em;
            border-radius: .25em;
            background-color: #EFE2F9;
            color: $primary;
        }
        &__bottom{
            display: flex;
            align-items: center;
            margin-top: .5em;
        }
        &__icon{
            width: 3em;
            flex-shrink: 0;
            margin-right: 1em;
            img{
                width: 100%;
                display: block;
            }
        }
        &__info{
            @include grid100gap(.25em);
        }
    }


    @media screen and (max-width: 576px){
        .achievement-item{
            grid-template-columns: 100%;
            padding-left: 1.75em;
        }
    }

</style>
