<template>
    <div class="footer-content">
        <span class="text">&copy;</span>
        <span class="k-logo"><span>k</span></span>
        <span class="text">2018</span>
    </div>
</template>

<style scoped>
    .k-logo {
        display: inline-block;
        width: 16px;
        height: 16px;
        color: #953043;
        background: #26262c;
        border-radius: 5px;
   }

    .k-logo span {
        position: relative;
        right: 2px;
        top: 1px;
    }

    .footer-content {
        position: absolute;
        bottom: 3px;
        left: 50%;
        transform: translateX(-50%);
        width: 100%;
        font-size: 13px;
        color: #3e3e46;
    }

    .text {
        line-height: 16px;
        vertical-align: top;
    }
</style>
