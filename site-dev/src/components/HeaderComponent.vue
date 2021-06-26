<template>
    <header>

        <nav class="container">

            <a href="http:/"><img id="logo" src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/wdev.svg
            " alt="Wdev"></a>

            <img id="menu-button" src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/menu.svg
            " alt="Abrir menu">

            <div id="menu-overlay"></div>

        </nav>
        
    </header>
</template>

<script>
export default {
    name : 'Header'
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
</style>