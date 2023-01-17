<template>
  <v-app dark>
    <v-navigation-drawer
      fixed
      app
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon >{{ item.icon }}</v-icon>
          </v-list-item-action>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar
      fixed
      app
    >
      <v-toolbar-title>{{ title }}</v-toolbar-title>
    </v-app-bar>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
    <v-footer
      :absolute="!fixed"
      app
    >
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data () {
    return {
      fixed: false,
      items: [
        {
          icon: 'mdi-account',
          title: 'Account',
          to: '/account'
        },
        {
          icon: 'mdi-calendar-multiple',
          title: 'calendar',
          to: '/calendar'
        }, 
        {
          icon: 'mdi-email',
          title: 'E-Mail',
          to: '/mail'
        }
        
      ],
      miniVariant: false,
      title: 'HWR AIO'
    }
  }
}
</script>