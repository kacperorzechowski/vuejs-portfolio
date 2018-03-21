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
          name: 'PHP 7.x',
          desc: 'I have knowledge of OOP in PHP.',
          level: 90
        },
        {
          name: 'Laravel 5.x.x',
          desc: 'Laravel is a PHP Framework. I work in it for almost a year. ' +
          'In my previous company we worked in Laravel with Lucid Architecture',
          level: 75
        },
        {
          name: 'Vue.js 2.x',
          desc: 'Vue.js is a JavaScript Framework.',
          level: 60
        },
        {
          name: 'Vanilla JavaScript',
          desc: 'Prototypal Inheritance and Functional Programming are hard, but very fascinating topics for me',
          level: 40
        },
        {
          name: 'CSS',
          desc: 'Knowledge of LESS and Bootstrap',
          level: 70
        },
        {
          name: 'RWD',
          desc: 'I am able to create Responsive Websites',
          level: 80
        },
        {
          name: 'SQL/Databases',
          desc: 'I have worked with Postgresql, MySql, Oracle and MSSQL',
          level: 50
        },
        {
          name: 'Linux',
          desc: 'Basic knowledge of Linux OS',
          level: 30
        }
      ]
    })
  }
</script>
<style scoped></style>
