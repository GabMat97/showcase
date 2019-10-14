<template>
    <!-- display the navigation bar -->
    <v-toolbar>
      <v-toolbar-items>
        <v-btn
          text
            tag='span'
            style='cursor: pointer'
            >
            SHOWCASE
        </v-btn>
      </v-toolbar-items>
      <v-spacer></v-spacer>
<!-- navigation bar links -->
      <v-toolbar-items class='hidden-xs-only'>
        <v-btn text v-for="item in items" :key="item.title" :to="item.link">
          <v-icon right>{{item.icon}}</v-icon>{{item.title}}
        </v-btn>
        <v-spacer></v-spacer>
      </v-toolbar-items>
      <!-- sign out button -->
      <v-toolbar-items class='hidden-xs-only'>
        <v-btn
          text
          >
          <v-icon right> </v-icon>Logout
        </v-btn>
      </v-toolbar-items>
    </v-toolbar>
</template>
<script>
export default {
  computed: {
    items() {
      let menuItems =  [
        {
          title: 'Register',
          icon: '',
          link: '/register'
        },
        {
          title: 'Login',
          icon: '',
          link: '/login'
        }
      ]
    return menuItems
    }
  }
}
</script>
