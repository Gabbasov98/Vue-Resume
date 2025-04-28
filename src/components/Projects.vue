<template>
    <div class="projects m-section">
        <div class="_line"></div>
        <div class="h2">
            Latest projects
        </div>

        <div class="projects__items">
            <div
                    class="project-item"
                    v-for="(item, index) in projectItems" :key="index"
            >
                <div class="project-item__top">
                    <div class="project-item__icon">
                        <img :src="$getImageUrl(item.icon)" alt="">
                    </div>
                    <div class="project-item__info">
                        <div class="project-item__name text16 medium-text">
                            {{item.name}}
                        </div>
                        <div class="project-item__desc text14 gray-text">
                            {{item.desc}}
                        </div>
                    </div>
                </div>
                <a target="_blank" :href="item.link" class="project-item__link">
                    <img src="../assets/img/chain2.svg" alt="">
                    <span class="text16">{{item.link}}</span>
                </a>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Projects",
        data() {
            return {
                projectItems: [
                    {
                        icon: "Wordpress.png",
                        name: "Rush Cloud site and WordPress admin-panel",
                        desc: "Web UI design for Rush Cloud",
                        link: "https://rushcloud.ru/",
                    },
                    {
                        icon: "Wordpress.png",
                        name: "Nordhan site and WordPress admin-panel",
                        desc: "Web UI design for Nordhan",
                        link: "https://nordhan.ru/",
                    },
                    {
                        icon: "Wordpress.png",
                        name: "Auditads site and WordPress admin-panel",
                        desc: "Web UI design for Auditads",
                        link: "https://auditads.ru/",
                    },
                    {
                        icon: "Wordpress.png",
                        name: "Bright Business site and WordPress admin-panel",
                        desc: "Web UI design for Bright Business",
                        link: "http://brightbusiness.pro/",
                    },
                ]
            }
        }
    }
</script>

<style scoped lang="scss">
    .projects{
        &__items{
            margin-top: 2em;
            display: grid;
            grid-template-columns: repeat(2,calc(50% - .375em));
            gap: .75em;
        }
    }

    .project-item{
        padding: 1.5em;
        background-color: $gray-light2;
        border-radius: .5em;
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        &__top{
            display: flex;
            align-items: flex-start;
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
        &__desc{
            letter-spacing: -.01em;
        }
        &__link{
            display: flex;
            align-items: center;
            font-family: $font2;
            font-weight: 600;
            color: #516CF7;
            &:hover{
                opacity: .8;
            }
            span{
                text-decoration: underline;
            }
            img{
                width: 1.5em;
                margin-right: .75em;
                flex-shrink: 0;
            }
        }
    }


    @media screen and (max-width: 576px){
        .projects{
            &__items{
                grid-template-columns: 100%;
            }
        }
    }

</style>
