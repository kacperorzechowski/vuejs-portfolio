<template>
    <div class="skill">
        <h2>{{ name }}</h2><br>
        <small>{{ desc }}</small>
        <div class="level">{{ level }}%</div>
    </div>
</template>
<script>
    export default {
        name: 'skill',
        props: {
            name: {
                type: String,
                default: 'Skill..'
            },
            desc : {
                type: String,
                default: 'Skill description'
            },
            img : {
                type: String,
                default: ''
            },
            level: {
                type: Number,
                default: 0
            }
        },
        data: () => ({
           showLevel: 0
        }),
        watch: {
            'level'(oldLevel, newLevel) {
                clearInterval(this.interval);

                if(newLevel === this.showLevel){
                    return;
                }

                this.interval = window.setInterval(function(){

                    if(this.showLevel !== newLevel){

                        var change = (newLevel - this.showLevel) / 10;

                        change = change >= 0 ? Math.ceil(change) : Math.floor(change);

                        this.showLevel = this.showLevel + change;

                    }

                }.bind(this), 20);
            }
        }
    }
</script>
<style scoped>
    .skill {
        width: 300px;
        height: 80px;
        display: inline-block;
        border: 2px solid #C62828;
        border-radius: 10px;
        text-align: left;
        padding: 10px;
        margin: 10px;
    }

    .level {
        position: relative;
        right: -75%;
        top: -50%;
        font-size: 36px;
        font-weight: 100;
    }
</style>