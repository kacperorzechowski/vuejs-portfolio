<template>
    <div class="sidebar">
        <ul>
            <li>
                <font-awesome-icon :icon="['fab', 'github']"/>
            </li>
            <li>
                <font-awesome-icon :icon="['fab', 'twitter']"/>
            </li>
            <li>
                <font-awesome-icon :icon="['fab', 'android']"/>
            </li>
            <li>
                <font-awesome-icon :icon="['fab', 'linkedin']"/>
            </li>
        </ul>
    </div>
</template>
<script>
  import FontAwesomeIcon from '@fortawesome/vue-fontawesome'
  import fontawesome from '@fortawesome/fontawesome'
  import brands from '@fortawesome/fontawesome-free-brands'

  export default {
    components: {
      FontAwesomeIcon
    }

  }
</script>
<style scoped>
    .sidebar {

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
