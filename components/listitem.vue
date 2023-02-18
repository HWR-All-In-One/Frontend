<template>
  <div>
    <v-list-group
      v-if="item.items !== undefined"
      v-model="item.active"
      :sub-group="isSubGroup"
      :class="isSubGroup ? 'right-icon' : ''"
    >
      <template v-slot:activator>
        <v-list-item-content>
          <v-list-item-title>
              <v-icon>{{ item.icon }}</v-icon>{{ item.title }}
          </v-list-item-title>
        </v-list-item-content>
      </template>
      <template v-for="subItem in item.items" >
        <list-item :item="subItem" :is-sub-group="true" :key="subItem.title">
        </list-item>
      </template>
    </v-list-group>
    <v-list-item v-else link router :to="item.to">
      <v-list-item-content>
        <v-list-item-title v-text="item.title"></v-list-item-title>
      </v-list-item-content>
    </v-list-item>
  </div>
</template>
<script>
export default {
  name: "listitem",
  props: ["item", "isSubGroup"],
  components: {
    ListItem: () => import("./listitem.vue"),
  },
};
</script>
<style>

.v-list-item__title{

color:red;
}
.test{

}

 .right-icon .v-list-group__header{
 width:max-content;
  display: flex !important;
  flex-direction: row-reverse !important;
 }
</style>