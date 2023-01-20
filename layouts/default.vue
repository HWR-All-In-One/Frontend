<template>
  <v-app dark>
    <v-navigation-drawer
      permanent
      width="5rem"
      fixed
      app
    >
      <div class="logo">
          <img src="../assets/logo-round-edition-WB.png" alt="HWR-APP-logo">
        </div>
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
      <v-toolbar-title
      permanent
      fixed
      width:15rem
      >{{ title }}
      </v-toolbar-title>
    </v-app-bar>
    <v-main>
      <v-container>
        <DropdownList />
      </v-container>
    </v-main>
    <v-footer
      :absolute="fixed"
      app
    >
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'app',
  
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
          to: '../pages/calendar.vue'
        }, 
        {
          icon: 'mdi-email',
          title: 'mail',
          to: '/mail'
        }
        
      ],
      miniVariant: false,
      title: 'HWR AIO'

    }
  }
}
</script> 

<style lang="scss">
  .v-navigation-drawer{
    display: flex;
    flex-direction: column;
  
    background-color: var(--dark);
    color: var(--light);

    .logo {
      position: relative;
      margin:0 0 50px;
      padding: 0.5rem;
      background:rgba(255,255,255,0);
      opacity: 5;
      

      img {
        height:4rem;
        width:4rem;
      }
    }
}
</style>
