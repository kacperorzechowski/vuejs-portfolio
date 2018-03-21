<template>
    <div class="welcome-content">
        <div class="me">
            <img src="../../../assets/me.jpg"/>
        </div>
        <div class="description">
            <span class="my-name">Hi, I am Kacper.</span>
            <span class="rest-info">
                I am 22 years old web developer living in Poland.
                I love both, Front-End and Back-End.
                My passion is also Game Developing, I have created and published an arcade android game.
                Currently I work as Full Stack web developer in my home city - Elbląg.
            </span>
        </div>
    </div>
</template>
<script>
    export default {
    }
</script>
<style scoped>

    .me {
        float: left;
    }

    .me img {
        width: 100px;
        height: 100px;
        border-radius: 51%;
        border: 3px solid #F1F1F1;
    }

    .description {
        display: inline-block;
        padding: 0 20px 0 20px;
        max-width: 550px;
        text-align: justify;
    }

    .description .my-name {
        display: block;
        font-weight: bold;
        font-size: 36px;
    }

    .description .rest-info {
        font-weight: 100;
        line-height: 1.3;
        word-spacing: 4px;
    }
</style>