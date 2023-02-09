<template>
  <v-app dark>
    <v-navigation-drawer
      permanent
      miniVariant
      mini-variant-width="5.3rem"
      v-model="drawer"
      :clipped="clipped"
      fixed
      app
    >
      <v-list>
        <div class="logo">
          <a class="home-link" href="/">
            <img src="~/assets/images/hwr_logo.svg" alt="HWR-APP-logo" />
          </a>
        </div>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <div class="theme-toggle-box">
          <v-switch
            class="theme-toggle"
            v-model="$vuetify.theme.dark"
            inset
            persistent-hint
          />
        </div>
      </v-list>
    </v-navigation-drawer>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
    <v-navigation-drawer>
      <v-list>
        <v-list-item>
          <v-list-item-action>
            <v-icon light> mdi-repeat </v-icon>
          </v-list-item-action>
          <v-list-item-title>Switch drawer</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-footer class="footer" fixed app>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
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
.theme.v-app-bar.v-toolbar.v-sheet {
  background-color: transparent;
}

.v-navigation-drawer {
  background-color: #363636;
  .logo {
    margin-bottom: 2rem;
    position: relative;
    background: rgba(255, 255, 255, 0);
    img {
      height: 5rem;
      width: 5rem;
    }
  }
}

.theme--dark.v-navigation-drawer:not(.v-navigation-drawer--floating)
  .v-navigation-drawer__border {
  background-color: #d50b2e;
}

.theme--light.v-navigation-drawer:not(.v-navigation-drawer--floating)
  .v-navigation-drawer__border {
  background-color: #d50b2e;
}

.v-navigation-drawer__border {
  width: 0.12rem;
}

.v-icon.v-icon {
  font-size: 2.1rem;
  color: #d50b2e;
}
.theme--dark.v-footer {
  background-color: transparent;
  color: #d50b2e;
}
.theme--light.v-footer {
  background-color: transparent;
  color: #d50b2e;
}
.theme--light.v-footer {
  background-color: transparent;
}
.footer {
  width: max-content;
}
</style>
