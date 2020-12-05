<template>
  <div class="text-center">
    <v-menu offset-y>
      <template v-slot:activator="{ on, attrs }">
        <v-btn
          color="primary"
          dark
          v-bind="attrs"
          v-on="on"
        >
          Pages
        </v-btn>
      </template>
      <v-list>
        <v-list-item
          v-for="(item, index) in items"
          :key="index"
          :href="item.href"
        >
          <v-list-item-title>{{ item.title }}</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-menu>
  </div>
</template>

<script>
  export default {
    name: "PublicNavigationDropdown",
    data: () => ({
      items: [
        { title: 'Home' , href:'/'},
        { title: 'About' , href:'/about'},
        { title: 'Discord' , href:'/discord'},
        { title: 'Steam' , href:'/steam'},
        { title: 'System Bar' , href:'/system-bar'},
        { title: 'Sidenav' , href:'/sidenav'},
        { title: 'Inbox' , href:'/inbox'},
        { title: 'Ext.Toolbar' , href:'/extended-toolbar'},
        { title: 'Constrained' , href:'/constrained'},
        { title: 'ThreeColumn' , href:'/three-column'}
      ],
    }),
  }
</script>