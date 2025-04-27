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

<style lang="scss">
    .skills{
        &__items{
            display: grid;
            grid-template-columns: repeat(3,calc(100% / 3 - 1em / 3));
            gap: .5em;
            margin-top: 2em;
        }
    }

    .skill-item{
        border-radius: .5em;
        background: #F7F9FC;
        padding: 1em 1.5em;
        display: flex;
        flex-direction: column;
        align-items: center;
        &__icon{
            height: 4em;
            flex-shrink: 0;
            margin-bottom: .5em;
            @include center;
            img{
                height: 100%;
                mix-blend-mode: multiply;
            }
        }
        &__date{
            margin-top: .2em;
        }
    }


    @media screen and (max-width: 576px){
        .skills{
            &__items{
                grid-template-columns: 100%;
            }
        }
    }

</style>
