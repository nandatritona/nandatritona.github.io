<template lang="">
    <footer>
        <div class="container">
            <div class="left">
                <div class="col-1">
                    <router-link class="header" :to="{ name: 'Home' }">IstiBlogs</router-link>
                    <ul>
                        <li>
                            <a href="#"><youTube class="svg-icon"/></a>
                        </li>
                        <li>
                            <a href="#"><twitter class="svg-icon"/></a>
                        </li>
                        <li>
                            <a href="#"><instagram class="svg-icon"/></a>
                        </li>
                        <li>
                            <a href="#"><linkedin class="svg-icon"/></a>
                        </li>
                    </ul>
                </div>
                <div class="col-2">
                    <ul>
                        <router-link class="link" :to="{ name: 'Home' }">About</router-link>
                        <router-link class="link" :to="{ name: 'press' }">Press</router-link>
                        <router-link v-if="user" class="link" :to="{ name: 'tips' }">Create Post</router-link>
                        <router-link v-if="!user" class="link" :to="{ name: 'team' }">Team Creative</router-link>
                    </ul>
                </div>
            </div>
            <div class="right">
                <p>Copyright 2022 All Rights Reserved</p>
            </div>
        </div>
    </footer>
</template>
<script>
import youTube from '../assets/Icons/youtube-brands.svg';
import twitter from '../assets/Icons/twitter-brands.svg';
import instagram from '../assets/Icons/instagram-brands.svg';
import linkedin from '../assets/Icons/linkedin-brands.svg';

export default {
    name: 'footer-vue',
    components: {
        youTube,
        twitter,
        instagram,
        linkedin
    },
};
</script>
<style lang="scss" scoped>
    footer {
        margin-top: auto;
        padding: 100px 25px;
        background-color: #303030;
        .container {
            display: flex;
            flex-direction: column;
            gap: 32px;
            @media (min-width: 800px) {
                flex-direction: row;
                gap: 0px;
            }
            > div {
                display: flex;
                flex: 1;
                // flex-direction: column;
                // gap: 32px;
                // @media (min-width: 800px) {
                //     flex-direction: row;
                //     gap: 0px;
                // }
            }
            .left {
                gap: 32px;
                color: aliceblue;
                display: flex;
                flex-direction: column;
                align-items: center;
                @media (min-width: 800px) {
                    flex-direction: row;
                    align-items: initial;
                    gap: 0;
                }
                .header {
                    text-align: center;
                    font-size: 26px;
                    color: #1eb8b8;
                    text-decoration: none;
                    font-weight: 600;
                    &:hover {
                       color: aliceblue;
                    }
                    @media(min-width: 800px) {
                        text-align: initial;
                    }
                }
                ul {
                    gap: 16px;
                    list-style: none;
                    display: flex;
                }
                .col-1,
                .col-2 {
                    gap: 32px;
                    display: flex;
                    flex: 1;
                    @media (min-width: 800px) {
                        gap: 0px;
                    }
                }
                .col-1 {
                    flex-direction: column;
    
                    h2 {
                        text-align: center;
                        @media (min-width: 800px) {
                            text-align: initial;
                        }
                    }
                    ul {
                        margin-top: auto;
                        li {
                            display: flex;
                            align-items: center;
                            .svg-icon {
                                height: 25px;
                                width: auto;
                                // margin-right: 8px;
                                color: aliceblue;
                            }
                        }
                    }
                }
    
                .col-2 {
                    ul {
                        height: 100%;
                        justify-content: center;
                        flex-direction: row;
                        flex-wrap: wrap;
                        @media (min-width: 800px) {
                           flex-direction: column;
                        }
                        .link {
                            font-size: 16px;
                            font-weight: 500;
                            color: aliceblue;
                            text-decoration: none;
                            &:hover {
                                color: #1eb8b8;
                            }
                        }
                    }
                }
            }
            .right {
                gap: 32px;
                color: aliceblue;
                align-items: center;
                flex-direction: column;
                @media (min-width: 800px) {
                    align-items: flex-end;
                    gap: 0;
                }
            }

            p {
                margin-top: auto;
            }
        }
    }
</style>