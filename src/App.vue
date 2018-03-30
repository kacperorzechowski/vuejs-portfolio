<template>
    <div id="app">
        <transition v-if="showMenus" name="fade" appear>
            <Navbar></Navbar>
        </transition>
        <transition v-if="showMenus" name="fade" appear>
            <Sidebar></Sidebar>
        </transition>
        <transition name="fade" appear>
            <router-view class="page-content" :class="{ safari: isSafari }"></router-view>
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
    computed: {
      isSafari() {
        return /^((?!chrome|android).)*safari/i.test(navigator.userAgent)
      }
    },
    mounted () {
      setTimeout(() => (this.showMenus = true), 2000)
    }
  }
</script>

<style>
    * {
        margin: 0;
    }

    #app {
        position: fixed;
        display: block;
        width: 100%;
        height: 100%;
        background: url('../static/images/nature.jpg') center no-repeat;
        -webkit-background-size: cover;
        background-size: cover;
        font-family: 'Avenir', Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #f1f1f1;
        overflow: hidden;
    }

    .navbar {
        display: block;
        width: auto;
        float: right;
        margin-right: 50px;
        margin-top: 50px;
    }

    .sidebar {
        position: absolute;
        top: 50%;
        transform: translateY(-50%);
        display: block;
        z-index: 3;
    }

    .page-content {
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        width: 100%;
        position: fixed;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        overflow-y: auto;
    }

    .fade-enter-active, .fade-leave-active {
        transition: opacity .7s;
    }

    .fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */
    {
        opacity: 0;
    }

    @media (max-width: 1024px) {
        .sidebar {
            right: 0;
        }
        .page-content {
            max-height: 80vh;
            top: 50%;
            transform: translate(-50%, -50%);
        }
        .safari {
            max-height: 70vh;
        }
        .navbar {
            margin-top: 20px;
            margin-right: 0;
            float: none;
        }
    }

    @media (max-width: 400px) {
        .navbar {
            top: initial;
            transform: initial;
        }

        .page-content {
            margin-top: 20px;
        }
    }

    @media (max-height: 400px) {
        .navbar {
            margin-top: 10px;
        }

        .page-content {
            max-height: 75vh;
        }
        .safari {
            max-height: 65vh;
        }
    }

    @media (max-height: 345px) {
        .page-content {
            max-height: 60vh;
        }
        .safari {
            max-height: 40vh;
        }
    }
</style>
