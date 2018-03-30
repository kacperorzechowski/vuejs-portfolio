<template>
    <div class="footer-content">
        <img style="width: 16px; height: 16px" src="../../../../static/icons/favicon-32x32.png"/>
        <span class="text">&copy; Kacper Orzechowski 2018</span>
    </div>
</template>

<style scoped>
    .footer-content {
        position: absolute;
        bottom: 3px;
        left: 50%;
        transform: translateX(-50%);
        width: 100%;
        font-size: 13px;
        color: #777;
    }

    .text {
        line-height: 16px;
        vertical-align: top;
    }
</style>
