<template>
    <div class="welcome-content">
        <div class="me">
            <img src="../../../../static/images/me.png"/>
            <span class="my-name">Hey, I am Kacper.</span>
        </div>
        <div class="description">
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
export default {}
</script>
<style scoped>

    .me {
        float: left;
        line-height: 100px;
    }

    .me img {
        width: 100px;
        height: 100px;
        border-radius: 51%;
        border: 3px solid #F1F1F1;
    }

    .me .my-name {
        font-size: 36px;
        vertical-align: top;
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
    @media(max-width: 1024px) {
        .description {
            font-size: 14px;
        }
        .me {
            float: none;
            margin: 0 auto;
        }

        .welcome-content {
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
        }
    }
    @media (max-width: 805px) {
        .welcome-content {
            width: 80vw;
            margin-left: -30px;
        }
    }

    @media (max-width: 500px) {
        .me img {
            display: block;
            height: 125px;
            width: 125px;
            position: relative;
            left: 50%;
            transform: translateX(-50%);
        }
        .me .my-name {
            font-size: 30px;
            text-align: left;

        }
        .me {
            line-height: 45px;
        }
    }

    @media (max-width: 333px) {
        .me .my-name {
            font-size: 26px;
        }
    }
</style>
