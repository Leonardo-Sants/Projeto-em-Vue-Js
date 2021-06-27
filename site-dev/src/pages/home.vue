<template>
    <main>

        <div class="text-top">Vídeos novos toda <b>quinta </b>às <b>20h</b></div>

        <a href="https://youtube.com/wdevoficial">
        <img src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/subscribe.svg" 
        alt="Inscreva-se" id="subscribe">
        </a>

        <div class="text-bottom">youtube.com/wdevoficial</div>

    </main>
</template>

<script>
export default {
    name: "Home"
}
</script>

<style scoped>
    main {
        background-color: var(--color-background-home);
        justify-content: center;
        align-items: center;
    }

    .text-top {
        color:  var(--color-text-light);
        margin-bottom: 20px;
    }

    #subscribe {
        width: 340px;
    }    

    @media (min-width: 700px){
        #subscribe {
            width: 400px;
    }
    }

    .text-bottom {
        color: var(--color-text-light);
        margin-top: 20px;
    }
</style>