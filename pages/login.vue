<template>
    <v-app>
        <NuxtLink class="login-button" to="/login/username">Anmelden</NuxtLink>
        <NuxtChild />

        <v-navigation-drawer v-model="rightDrawer" :right="right" temporary fixed>
            <v-list>
                <v-list-item @click.native="right = !right">
                    <v-list-item-action>
                        <v-icon light>
                            mdi-repeat
                        </v-icon>
                    </v-list-item-action>
                    <v-list-item-title>Switch drawer (click me)</v-list-item-title>
                </v-list-item>
            </v-list>
        </v-navigation-drawer>
    </v-app>
</template>

<script>
import UsernameField from '~/components/UsernamePanel.vue';

export default {
    name: "DefaultLayout",
    data() {
        return {
            clipped: false,
            drawer: false,
            fixed: false,
            items: [
                {
                    icon: "mdi-apps",
                    title: "Welcome",
                    to: "/"
                },
                {
                    icon: "mdi-chart-bubble",
                    title: "Inspire",
                    to: "/inspire"
                }
            ],
            miniVariant: false,
            right: true,
            rightDrawer: false,
            title: "Vuetify.js"
        };
    },
    components: {
        UsernameField
    }
}
</script>

<style lang="scss">
/* Dark Theme Styling */


/* Light Theme Styling */


/* General Mobile Styling */


/* General Desktop Styling */
.login-button,
.registration-button {
    display: flex;
    justify-content: center;
    text-decoration: none;
    margin-bottom: 1rem;
}

</style>
