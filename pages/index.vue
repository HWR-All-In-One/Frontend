<template>
    <v-app>
        <div>
            <h1 class="main-title">
                Hauptseite
            </h1>
            <v-btn color="primary" nuxt to="/login/username">
                Login
            </v-btn>
        </div>
    </v-app>
</template>

<script>
export default {
    name: 'IndexPage',
}
</script>

<style lang="scss">
/* Dark Theme Styling */


/* Light Theme Styling */


/* General Mobile Styling */


/* General Desktop Styling */
.main-title {
    padding: 50px 0 25px 0;
}

.login-button,
.registration-button {
    display: flex;
    justify-content: center;
    text-decoration: none;
    margin-bottom: 1rem;
}
</style>
