<template>
    <main>
        <div class="text-top">
            VÍDEOS NOVOS TODA <b>QUINTA</b> ÀS 20H
        </div>

        <a href="youtube.com" target="_blank">
            <img alt="Inscreva-se" id="subscribe" src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/subscribe.svg"/>
        </a>

        <div class="text-bottom">
            youtube.com/matheus
        </div>
    </main>
</template>

<script>
    export default {
        name: 'HomePage',
        
    }
</script>

<style scoped>

    main{
        background-color: var(--color-background-home);
        justify-content: center;
        align-items: center;
    }

    .text-top{
        font-size: 22px;
        color: var(--color-text-light);
        text-align: center;
        margin-bottom: 20px;
    }

    .text-bottom{
        font-size: 16px;
        color: var(--color-text-light);
        text-align: center;
        margin-top: 20px;
    }

    #subscribe{
        width: 200px;
        display: block;
        margin: 0 auto;
    }

    @media (min-width: 700px){
        #subscribe{
            width: 400px;
        }
    }

</style>