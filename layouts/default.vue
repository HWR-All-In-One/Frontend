<template>
  <v-app dark>
    <v-navigation-drawer
      permanent
      miniVariant
      mini-variant-width="5.3rem"
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      app
    >
      <v-list>
       <div class="logo">
          <img src="../assets/HWR-AIO-lOGO.svg" alt="HWR-APP-logo" />
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
      </v-list>
    </v-navigation-drawer>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
    <v-navigation-drawer v-model="rightDrawer" :right="right" temporary fixed>
      <v-list>
        <v-list-item @click.native="right = !right">
          <v-list-item-action>
            <v-icon light> mdi-repeat </v-icon>
          </v-list-item-action>
          <v-list-item-title>Switch drawer (click me)</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-footer :absolute="!fixed" app>
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
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
         {
          icon: "mdi-account",
          title: "Account",
          to: "/account"
        },
        {
          icon: "mdi-calendar-multiple",
          title: "calendar",
          to: "../pages/calendar.vue"
        },
        {
          icon: "mdi-email",
          title: "mail",
          to: "/mail"
        },
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: "HWR All-In-One",
    };
  },
};
</script>

<style lang="scss">
.theme--dark.v-app-bar.v-toolbar.v-sheet {
  background-color: transparent;
}

.v-list .v-list-item--active
{
    margin-top:5rem;
}
.v-navigation-drawer {
  background-color: #363636;

  .logo {
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

.v-navigation-drawer__border {
  width: 0.12rem;
}


.v-icon.v-icon {
  font-size: 2.1rem;
}

.theme--dark.v-footer {
  background-color: transparent;
}

.theme--light.v-footer {
  background-color: transparent;
}


</style>