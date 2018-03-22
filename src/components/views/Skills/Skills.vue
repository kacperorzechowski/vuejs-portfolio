<template>
    <div class="skills">
        <!--<Skill v-for="skillInfo in skills" v-bind="skillInfo"></Skill>-->
        <div class="languages">
            <div class="heading">
                <font-awesome-icon class="icon" :icon="faPlus"/>
                Languages
            </div>
            <ul>
                <li v-for="language in languages">
                    <div class="skill-name">{{ language.name }}</div>
                    <div>
                        <LevelProgress :value="language.level"></LevelProgress>
                        <div class="level">{{ language.level }}%</div>
                    </div>
                </li>
            </ul>
        </div>
        <div class="frameworks">
            <div class="heading">
                <font-awesome-icon class="icon" :icon="faPlus"/>
                Frameworks/Libraries
            </div>
            <ul>
                <li v-for="framework in frameworks">
                    <div class="skill-name">{{ framework.name }}</div>
                    <div>
                        <LevelProgress :value="framework.level"></LevelProgress>
                        <div class="level">{{ framework.level }}%</div>
                    </div>
                </li>
            </ul>
        </div>
    </div>
</template>
<script>
    import Skill from '../../domains/Skills/Skill.vue'
    import LevelProgress from '../../domains/Skills/LevelProgress.vue'
    import FontAwesomeIcon from '@fortawesome/vue-fontawesome'
    import faPlus from '@fortawesome/fontawesome-free-solid/faPlus'

    export default {
        name: 'Skills',
        components: {Skill, FontAwesomeIcon, LevelProgress},
        data: () => ({
            languages: [
                {
                    name: 'PHP 5.6, 7.0+',
                    level: 90
                },
                {
                    name: 'Vanilla JavaScript',
                    level: 40
                },
                {
                    name: 'HTML5',
                    level: 90
                },
                {
                    name: 'CSS3',
                    level: 80
                },
                {
                    name: 'SQL, PL/SQL',
                    level: 60
                }

//                {
//                    name: 'RWD',
//                    desc: 'I am able to create Responsive Websites',
//                    level: 80
//                },
//                {
//                    name: 'GIT',
//                    desc: 'I am familiar with Version Control System like GIT',
//                    level: 60
//                },
//                {
//                    name: 'SQL/Databases',
//                    desc: 'I have worked with Postgresql, MySql, Oracle and MSSQL',
//                    level: 50
//                },
//                {
//                    name: 'Linux',
//                    desc: 'Basic knowledge of Linux Ecosystem',
//                    level: 30
//                }
            ],
            frameworks: [
                {
                    name: 'Laravel 5.6+',
                    level: 75
                },
                {
                    name: 'Vue.js 2.x',
                    level: 60
                },
                {
                    name: 'Bootstrap',
                    level: 70
                },
                {
                    name: 'jQuery',
                    level: 60
                },
            ]
        }),
        computed: {
            faPlus() {
                return faPlus
            }
        }
    }
</script>
<style scoped>
    .languages, .frameworks {
        min-width: 400px;
    }

    .heading {
        color: #C62828;
        font-weight: bold;
        font-size: 28px;
    }

    .heading .icon {
        font-size: 10px;
        vertical-align: middle;
        padding: 5px;
    }

    ul {
        list-style: none;
    }

    ul li {
        text-transform: uppercase;
        font-size: 24px;
        padding: 10px 0 10px 0;
    }

    .skills {
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        text-align: left;
        justify-content: flex-end;
    }

    .level {
        display: inline-block;
        font-size: 14px;
        vertical-align: top;
        padding: 6px;
    }

    .skill-name {
        font-size: 18px
    }

    @media(max-width: 1024px) {
        .heading {
            font-size: 20px;
            margin-left: 20px;
        }
        .skill-name {
            font-size: 14px;
        }
    }
    @media(max-width: 374px) {
        .skills {
            margin-left: 30px;
        }
    }
</style>
