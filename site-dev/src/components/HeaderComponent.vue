<template>
    <header>

        <nav class="container">

            <router-link to="/"><img id="logo" src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/wdev.svg
            " alt="Wdev"></router-link>

            <img @click="openMenu" id="menu-button" src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/menu.svg
            " alt="Abrir menu">

            <div @click="closeMenu" id="menu-overlay" v-if="menuActive"></div>

            <div id="menu-items" :class="{active: menuActive}">

                <a href="http:/"><img id="menu-logo" src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/wdev.svg
                " alt="Wdev"></a>

                <ul>
                    <li @click="closeMenu"><router-link to="/">Home</router-link></li>
                    <li @click="closeMenu"><router-link to="/Videos">Vídeo</router-link></li>
                    <li @click="closeMenu"><router-link to="/sobre">Sobre</router-link></li>
                    <li @click="closeMenu"><router-link to="/contato">Contato</router-link></li>
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
    display: flex;
}

#menu-button {
    width: 30px;
}

.container {
    width: 90%;
    align-items: center;
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
}

ul li a {
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