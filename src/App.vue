<template>
    <div id="app">
        <transition v-if="showMenus" name="fade" appear>
            <div>
                <Navbar></Navbar>
                <Sidebar></Sidebar>
            </div>
        </transition>
        <transition name="fade" appear>
            <router-view class="page-content"></router-view>
        </transition>
        <Footer></Footer>
    </div>
</template>

<script>
    import Welcome from './components/views/Welcome/Welcome.vue'
    import Navbar from './components/domains/Navigation/Navbar.vue'
    import Footer from './components/domains/Footer/Footer.vue'
    import Sidebar from './components/domains/Sidebar/Sidebar.vue'

    export default {
        name: 'app',
        components: {
            Welcome,
            Navbar,
            Footer,
            Sidebar
        },
        data: () => ({
            showMenus: false
        }),
        mounted() {
            setTimeout(() => (this.showMenus = true), 2000)
        }
    }
</script>

<style>
    * {
        margin: 0;
    }

    #app:before {
        content: "";
        position: fixed;
        z-index: -1;
        left: 0;
        top: 0;
        display: block;
        width: 100%;
        height: 100%;
        background: url('./assets/nature.jpg') center no-repeat;
        -webkit-background-size: cover;
        background-size: cover;
        filter: grayscale(55%);
    }

    #app {
        font-family: 'Avenir', Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #f1f1f1;
        height: 100vh;
        background: rgba(33, 27, 27, 0.9);
        overflow: hidden;
    }

    .page-content {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
    }

    .fade-enter-active, .fade-leave-active {
        transition: opacity .7s;
    }

    .fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */
    {
        opacity: 0;
    }
</style>
