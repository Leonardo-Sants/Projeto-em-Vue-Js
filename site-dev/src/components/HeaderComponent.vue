<template>
    <header>

        <nav class="container">

            <a href="http:/"><img id="logo" src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/wdev.svg
            " alt="Wdev"></a>

            <img @click="openMenu" id="menu-button" src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/menu.svg
            " alt="Abrir menu">

            <div @click="closeMenu" id="menu-overlay" v-if="menuActive"></div>

            <div id="menu-items" :class="{active: menuActive}">

                <a href="http:/"><img id="menu-logo" src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/wdev.svg
                " alt="Wdev"></a>

                <ul>
                    <li><a href="/"></a>Home</li>
                    <li><a href="/video"></a>Vídeo</li>
                    <li><a href="/sobre"></a>Sobre</li>
                    <li><a href="/contato"></a>Contato</li>
                </ul>

            </div>

        </nav>
        
    </header>
</template>

<script>
export default {
    name : 'Header',
    data() {
        return {
            menuActive: false
        }
    },
    methods: {
        openMenu: function (){
            this.menuActive = true;
        },
        closeMenu: function (){
            this.menuActive = false;
        }
    }
}
</script>

<style scoped>
header {
    background-color: var(--color-background-nav);
    width: 100%;
    height: 60px;
    display: flex;
    justify-content: center;
    align-items: center;
}

nav {
    display: flex;
    justify-content: space-between;
}

#logo {
    width: 130px;
}

#menu-button {
    width: 30px;
}

.container {
    width: 90%;
}

#menu-overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 40%;
    height: 100vh;
    background-color: #000000;
    opacity: 0.8;
}

#menu-items {
    position: fixed;
    top: 0;
    right: 0;
    background-color: var(--color-background-nav);
    width: 60%;
    height: 100vh;
    display: none;
    flex-direction: column;
    align-items: center;
}

#menu-items.active {
    display: flex;
}

#menu-logo {
    width: 110px;
    margin: 30px;
}

ul {
    list-style: none;
    text-align: center;
}

ul li {
    margin: 20px 0px;
    color: var(--color-text-light);
}

@media (min-width: 700px) {
    #menu-button,
    #menu-logo,
    #menu-overlay {
        display: none;
    }

    #menu-items {
        display: flex;
        position: static;
        height: 60px;
        width: auto;
    }

    ul {
        display: flex;
        height: 60px;
        align-items: center;
    }

    ul li {
        margin: 0;
        margin-left: 20px;
    }
}

</style>