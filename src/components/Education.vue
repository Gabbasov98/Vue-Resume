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

<style lang="scss">
    .education{
        &__items{
            display: grid;
            grid-template-columns: repeat(2,calc(50% - .375em));
            gap: .75em;
            margin-top: 2em;
        }
    }

    .education-item{
        border-radius: .5em;
        background: #F7F9FC;
        padding: 1em 1.5em;
        &__top{
            display: flex;
            align-items: center;
            margin-bottom: .5em;
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
        &__date{
            margin-top: .2em;
        }
    }


    @media screen and (max-width: 992px){
        .education{
            margin-top: 3em;
        }
    }

    @media screen and (max-width: 576px){
        .education{
            &__items{
                grid-template-columns: 100%;
            }
        }
    }

</style>
