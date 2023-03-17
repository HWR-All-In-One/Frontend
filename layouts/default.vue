<template>
    <v-app>
        <v-navigation-drawer permanent miniVariant mini-variant-width="5.5rem" fixed app>
            <v-list class="navbar">
                <div class="logo">
                    <NuxtLink class="home-link" to="/">
                        <img src="~/assets/images/hwr_logo.svg" alt="HWR-APP-logo" />
                    </NuxtLink>
                </div>
                <v-list-item v-for="(item, i) in items" :key="i" :to="item.to" router exact>
                    <v-list-item-action>
                        <v-icon>
                            {{ item.icon }}
                        </v-icon>
                    </v-list-item-action>
                    <v-list-item-content>
                        <v-list-item-title>
                            {{ item.title }}
                        </v-list-item-title>
                    </v-list-item-content>
                </v-list-item>
            </v-list>
            <div class="theme-toggle">
                <v-list-item class="theme-toggle-icon">
                    <v-icon class="mdi mdi-theme-light-dark" />
                </v-list-item>
                <v-list-item class="theme-toggle-item">
                    <v-switch class="theme-toggle-switch" v-model="$vuetify.theme.dark" inset persistent-hint />
                </v-list-item>
            </div>
        </v-navigation-drawer>
        <v-main>
            <v-container>
                <Nuxt />
            </v-container>
        </v-main>
    </v-app>
</template>

<script>
export default {
    name: "app",
    name: "DefaultLayout",
    data() {
        return {
            items: [
                {
                    icon: "mdi-account",
                    title: "Benutzerkonto",
                    to: "/login/username"
                },
                {
                    icon: "mdi-calendar-multiple",
                    title: "Stundenplan",
                    to: "/schedule"
                },
                {
                    icon: "mdi-email",
                    title: "Email-Postfach",
                    to: "/mail"
                }
            ]
        };
    }
};
</script>

<style lang="scss">
/* Dark Theme Styling */
.theme--dark.v-navigation-drawer:not(.v-navigation-drawer--floating) .v-navigation-drawer__border {
    background-color: $color-hwr-red;
}

/* Light Theme Styling */
.theme--light.v-navigation-drawer:not(.v-navigation-drawer--floating) .v-navigation-drawer__border {
    background-color: $color-hwr-red;
}

/* General Mobile Styling */


/* General Desktop Styling */
.theme.v-app-bar.v-toolbar.v-sheet {
    background-color: transparent;
}

.v-navigation-drawer {
    background-color: $color-dark-mode;

    .v-list {
        max-height: 100vh;
        position: absolute;

        .logo {
            position: relative;
            margin-bottom: 2rem;

            img {
                height: 5rem;
                width: 5.4rem;
            }
        }
    }
}

.v-navigation-drawer__border {
    width: 0.12rem;
}

.v-icon.v-icon {
    font-size: 2.1rem;
    color: $color-hwr-red;
}

.navbar {
    position: relative;
}

.theme-toggle {
    position: absolute;
    bottom: 0.5rem;
    left: 0.7rem;
}

.theme-toggle-switch {
    position: absolute;
    left: -0.7rem;
    -moz-transform: scale(-1, 1);
    -webkit-transform: scale(-1, 1);
    -o-transform: scale(-1, 1);
    -ms-transform: scale(-1, 1);
    transform: scale(-1, 1);
}
</style>
