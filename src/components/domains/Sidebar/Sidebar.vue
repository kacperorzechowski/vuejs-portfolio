<template>
    <div class="sidebar">
        <ul>
            <li>
                <a href="https://github.com/kacperorzechowski"><font-awesome-icon :icon="['fab', 'github']"/></a>
            </li>
            <li>
                <a href="https://twitter.com/k_orzechowski96"><font-awesome-icon :icon="['fab', 'twitter']"/></a>
            </li>
            <li>
                <a href="https://play.google.com/store/apps/details?id=com.KacperOrzechowski.dragSquare"><font-awesome-icon :icon="['fab', 'android']"/></a>
            </li>
            <li>
                <a href="https://www.linkedin.com/in/kacperorzechowski/"><font-awesome-icon :icon="['fab', 'linkedin']"/></a>
            </li>
        </ul>
    </div>
</template>
<script>
  import FontAwesomeIcon from '@fortawesome/vue-fontawesome'
  import brands from '@fortawesome/fontawesome-free-brands'

  export default {
    components: {
      FontAwesomeIcon
    }

  }
</script>
<style scoped>
    a, a:visited, a:active, a:link {
        color: #b6b6b6;
    }

    ul {
        list-style: none;
    }

    ul li {
        font-size: 36px;
        padding: 20px;
    }

    ul li svg:hover {
        color: #C62828;
        transition-duration: 0.3s;
    }
</style>
