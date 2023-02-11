<template>
    <v-app>
        <v-navigation-drawer permanent miniVariant mini-variant-width="5.5rem" fixed app>
            <v-list>
                <div class="logo">
                    <a class="home-link" href="/">
                        <img src="~/assets/images/hwr_logo.svg" alt="HWR-APP-logo" />
                    </a>
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
                <v-list-item class="theme-icon">
                    <v-icon class="mdi mdi-theme-light-dark"/>
                </v-list-item>
                <v-list-item class="theme-toggle-item">
                    <div class="theme-toggle-box">
                        <v-switch class="theme-toggle" v-model="$vuetify.theme.dark" inset persistent-hint />
                    </div>
                </v-list-item>
            </v-list>
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
                    to: "/account"
                },
                {
                    icon: "mdi-calendar-multiple",
                    title: "Kalender",
                    to: "/calendar"
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
    background-color: #363636;

    .v-list {
        height: 100vh;
        position: absolute;

        .logo {
            position: relative;
            margin-bottom: 2rem;
            background: rgba(255, 255, 255, 0);

            img {
                height: 5rem;
                width: 5.4rem;
            }
        }

        .theme-icon {
            margin-left: 0.7rem;
            position: absolute;
            bottom: 3rem;
        }

        .theme-toggle-item {
            margin-left: 0.5rem;
            position: absolute;
            bottom: 0;
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

.theme-toggle-item {
    margin-left: 1rem;
}
</style>
