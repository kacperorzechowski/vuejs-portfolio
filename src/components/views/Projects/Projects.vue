<template>
    <div class="projects">
        <div class="project">
            <div class="header">
                <div class="type work-project">Work project</div>
                <div class="name">Point Of Sale - sales system</div>
            </div>
            <div class="stack"><span class="label">Tech stack: </span>Laravel (Lucid architecture), Vue.js, Node.js, HTML/CSS, Postresql</div>
            <div class="desc">
                POS is a sale system which using Node.js to communicate with receipt printer.
                Salesman is operating on Vue.js interface that communicates with Laravel which is providing and receiving data.
                After validation Laravel sends request to Node to print the receipt.
            </div>
            <div class="period">March 2018 - currently</div>
        </div>

        <div class="project">
            <div class="header">
                <div class="type work-project">Work project</div>
                <div class="name">Viola Kiosk</div>
            </div>
            <div class="stack"><span class="label">Tech stack: </span>Laravel (Lucid architecture), Vue.js, HTML/CSS, SQL, Postresql</div>
            <div class="desc">
                Viola Kiosk is an autonomous system that offers browsing and ordering company's products.
                Kiosk runs on Raspberry PI and has touch screen which makes client able to controller app more easily.
                Firstly, the Front End of application was written in Laravel Blades but afterwards we decided to rewrite it
                as Single Page Application in Vue.js.
            </div>
            <div class="period">August 2017 - March 2018</div>
        </div>

        <div class="project">
            <div class="header">
                <div class="type personal-project">Personal project</div>
                <div class="name">
                    Drag Square
                    <a href="https://play.google.com/store/apps/details?id=com.KacperOrzechowski.dragSquare">
                        <FontAwesomeIcon class="icon" :icon="faVisit"/>
                    </a>
                </div>
            </div>
            <div class="stack"><span class="label">Tech stack: </span>C#, Unity3D</div>
            <div class="desc">
                Drag Square was my first mobile game written in C# using Unity3D engine. The Drag Square is a simple arcade
                game for Android. The point of the game is to keep little square on screen. You get score every time you collide
                with square on the middle.
            </div>
            <div class="period">March 2017</div>
        </div>

        <div class="project">
            <div class="header">
                <div class="type personal-project">Personal project</div>
                <div class="name">Onlywar.eu - CS:GO Servers network</div>
            </div>
            <div class="stack"><span class="label">Tech stack: </span>PHP, MyBB, HTML/CSS, SQL, MySQL, Sourcemod/Pawno, SRCDS</div>
            <div class="desc">
                Onlywar.eu (before cs-go4fun.pl) was popular multiplayer servers network for Counter Strike: Global Offensive.
                As owner I was responsible for anything. From creating modifications through server configuration to Social Media
                or PR. I learned a lot back then. In best times there were 3 game servers, TeamSpeak3 server and a big community board with
                automated shop that was offering premium features. <span class="important">On February 2017 I have sold the whole network and I am not
                associated with it anymore</span>.
            </div>
            <div class="period">September 2014 - February 2017</div>
        </div>
    </div>
</template>

<script>
  import FontAwesomeIcon from '@fortawesome/vue-fontawesome'
  import faVisit from '@fortawesome/fontawesome-free-solid/faExternalLinkAlt'

  export default {
      name: 'Projects',
      components: {FontAwesomeIcon},
      computed: {
        faVisit() {
          return faVisit
        }
      }
    }
</script>

<style scoped>
    .projects {
        display: inline-block;
        max-width: 80vw;
    }

    .project {
        max-width: 400px;
        display: inline-block;
        padding: 15px;
        vertical-align: top;
        text-align: left;
        margin-bottom: 10px;
    }

    .header {
        min-height: 45px;
        margin-bottom: 10px;
    }

    .type {
        display: inline-block;
        font-weight: bold;
        font-size: 15px;
        padding: 5px;
        border-radius: 5px;
        width: 30%;
        text-align: center;
        float: right;
    }

    .work-project {
        background: #1DE9B6;
        color: #000;
    }

    .personal-project {
        background: #BA68C8;
        color: #fff;
    }

    .name {
        display: inline-block;
        width: 65%;
        font-weight: bold;
        font-size: 20px;
    }

    .name a {
        color: #f44336;
    }

    .name a:hover {
        color: #C62828;
        transition-duration: 0.3s
    }

    .stack .label {
        font-weight: bold;
    }

    .stack {
        margin-bottom: 10px;
    }

    .desc {
        color: #c5c5c5;
        font-size: 15px;
    }

    .period {
        font-style: italic;
        font-size: 14px;
        float: right
    }

    .important {
        color: #F4511E;
    }

    @media (max-width: 400px) {
        .projects {
            margin-left: -30px;
        }

        .project:not(:last-child) {
            border-bottom: 1px solid rgba(74, 48, 46, 0.6);
        }
    }
</style>
