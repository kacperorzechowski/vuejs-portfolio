<template>
    <div class="skills">
        <Skill v-for="skillInfo in skills" v-bind="skillInfo"></Skill>
    </div>
</template>
<script>
    import Skill from '../../Skill.vue'

    export default {
        name: 'Skills',
        components: {Skill},
        data: () => ({
            skills: [
                {
                    name: 'Laravel 5.x.x',
                    desc: 'Laravel is a PHP Framework.',
                    img: '',
                    level: 80
                },
                {
                    name: 'Vue.js 2.x.x',
                    desc: 'Vue.js is a JavaScript Framework.',
                    img: '',
                    level: 50
                },
                {
                    name: 'Laravel 5.x.x',
                    desc: 'Laravel is a PHP Framework.',
                    img: '',
                    level: 80
                },
                {
                    name: 'Vue.js 2.x.x',
                    desc: 'Vue.js is a JavaScript Framework.',
                    img: '',
                    level: 50
                }
            ]
        })
    }
</script>
<style scoped></style>