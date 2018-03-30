<template>
    <div class="contact">
        <div class="method">
            <div class="icon">
                <font-awesome-icon class="icon" :icon="faPhone"/>
            </div>
            <div class="label"><span class="flag"></span>+48 500 131 704</div>
            <div class="short-desc">Call or text me :)</div>
        </div>
        <div class="method">
            <div class="icon">
                <font-awesome-icon class="icon" :icon="faEnvelope"/>
            </div>
            <div class="label">kacper.orzechowski96@gmail.com</div>
            <div class="short-desc">Want know more? Kindly mail me and I will answer you asap.</div>
        </div>
    </div>
</template>

<script>
    import FontAwesomeIcon from '@fortawesome/vue-fontawesome'
    import faPhone from '@fortawesome/fontawesome-free-solid/faPhone'
    import faEnvelope from '@fortawesome/fontawesome-free-solid/faEnvelope'

    export default {
      name: 'Contact',
      components: {FontAwesomeIcon},
      computed: {
        faPhone() {
          return faPhone
        },
        faEnvelope() {
         return faEnvelope
        }
      }
    }
</script>

<style scoped>
    .contact {
        display: inline-block;
        max-width: 80vw;
    }

    .contact .method {
        display: inline-block;
        vertical-align: top;
        width: 250px;
        margin: 20px;
    }

    .icon {
        font-size: 48px;
        color: #C62828;
    }

    .flag {
        display: inline-block;
        width: 16px;
        border-top: 5px solid white;
        border-bottom: 5px solid red;
        margin-right: 4px;
    }

    .label {
        margin-top: 10px;
        margin-bottom: 10px;
        color: #B71C1C;
        font-weight: bold;
    }

    .short-desc {
        max-width: 250px;
        color: #c5c5c5;
        font-size: 15px;
    }

    @media (max-width: 400px) {
        .contact .method {
            width: 200px;
            margin-left: -30px;
        }

        .icon {
            font-size: 36px;
        }

        .label {
            font-size: 12px;
        }

        .short-desc {
            font-size: 11px;
            width: 200px;
        }
    }
</style>
