s<template>
  <v-app>
    <v-navigation-drawer
      permanent
      mini-variant
      fixed
      app
    >
      
      <v-list>  
        <div class="logo">
          <img src="../assets/HWR-lOGO-3-with-bear-symbol-small-lightmode.svg" alt="HWR-APP-logo">
        </div>

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
      
    <v-main>
      <v-container>
        <DropdownList />
      </v-container>
    </v-main>
  
    <v-row>
      <v-btn
        :loading="loading3"
        :disabled="loading3"
        color="blue-grey"
        class="button1"
        @click="loader = 'loading3'"
      >
        Heute
      </v-btn>
      <v-btn
        :loading="loading3"
        :disabled="loading3"
        color="blue-grey"
        class="button2"
        @click="loader = 'loading3'"
      >
        Wochen
      </v-btn>
      <v-btn
        :loading="loading3"
        :disabled="loading3"
        color="blue-grey"
        class="button3"
        @click="loader = 'loading3'"
      >
        Monate
      </v-btn>
      <v-btn
        :loading="loading3"
        :disabled="loading3"
        color="blue-grey"
        class="button4"
        @click="loader = 'loading3'"
      >
        Jahr
      </v-btn>
    </v-row>
  
    <v-footer app bottom fixed style="width: max-content;" padless>
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

.theme--dark.v-app-bar.v-toolbar.v-sheet {
    background-color: transparent;
}
.theme--light.v-app-bar.v-toolbar.v-sheet {
    background-color: transparent;
    border:none;
}
  .theme--dark.v-navigation-drawer {
    background-color: grey;
    border: none;
    

    .logo {
      position: relative;
      margin:auto;
      
      padding: auto;
      background:rgba(255,255,255,0);
      opacity: 6;
      
      img {
        height:3rem;
        width:3rem;
      }
    }
  }

  .theme--light.v-navigation-drawer {
    background-color: transparent;
    border: none;
    

    .logo {
      position: relative;
      margin:0 0;
      padding: 0.5rem;
      
      opacity: 5;
      
      img {
        height:3rem;
        width:3rem;
      }
    }
  }

  .theme--dark.v-footer {
    background-color: transparent;
  }

  .theme--light.v-footer {
    background-color: transparent;
  }
  
  .v-toolbar__title, .v-toolbar__content{
    block-size: max-content;
    
  }

 .row{
  margin: auto 1rem auto auto;
  flex: initial;
  height: max-content;
 }

 .button1 {
  background-color: #4CAF50;
  border: none;
  color: white;
  padding: 30px 60px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  margin: auto 1rem 1rem auto;
  cursor: pointer;
}

</style>
