<template>

    <v-toolbar flat class="mainHeader"> 
      
      <v-toolbar-title>Click Motto</v-toolbar-title>

        <v-spacer></v-spacer>
          <v-toolbar-items class="hidden-xs-only">

            <v-btn text class="navtext">
              Explore
            </v-btn>

            <v-btn text class="navtext">
              Discover
            </v-btn>

            <v-btn text class="navtext">
              For Professionals
            </v-btn>


              <v-menu bottom left>
              <template v-slot:activator="{ on, attrs }">
                <v-btn
                
                  icon
                  v-bind="attrs"
                  v-on="on"
                >
                  <v-icon>mdi-dots-horizontal</v-icon>
                </v-btn>
              </template>

              <v-list class="dropclass">
                <v-list-item
                  v-for="(item, i) in items"
                  :key="i"
                >
                  <v-list-item-title class="dropclassfont">{{ item.title }}</v-list-item-title>
                </v-list-item>
              </v-list>
            </v-menu>
  
            <div style="margin-top: 14px; margin-left: 10px; margin-right: 20px;">
            <v-btn outlined color="black" class="navtext">
              Submit Photos
            </v-btn>
            </div>
            <div style="border-right: 1px black solid; margin-top: 5px;"></div>

            <v-btn text class="navtext ">
              <div class="vl"></div>
              Login
            </v-btn>

            <div style="margin-top: 14px;">
            <v-btn color="warning" dark class="navtext">
              Join Free
            </v-btn>
            </div>

      </v-toolbar-items>
      

      <div class="hidden-sm-and-up">
        <v-menu offset-y>
          <template v-slot:activator="{ on }">
            <v-app-bar-nav-icon v-on="on"></v-app-bar-nav-icon>
          </template>
          <v-list class="responsiveMenu">
            <v-list-item>
              <v-list-item-title><router-link to="/">Explore</router-link></v-list-item-title>
            </v-list-item>
            <v-list-item>
              <v-list-item-title><router-link to="/">Discover</router-link></v-list-item-title>
            </v-list-item>
            <v-list-item>
              <v-list-item-title><router-link to="/">For Professionals</router-link></v-list-item-title>
            </v-list-item>
            <v-list-item>
              <v-list-item-title><router-link to="/">Submit Photos</router-link></v-list-item-title>
            </v-list-item>
            <v-list-item>
              <v-list-item-title><router-link to="/">Login</router-link></v-list-item-title>
            </v-list-item>
            <v-list-item>
              <v-list-item-title><router-link to="/">Join Free</router-link></v-list-item-title>
            </v-list-item>
          </v-list>
        </v-menu>
      </div>


    </v-toolbar>
  
</template>

<script>
  export default {
    name: 'Header',

    data: () => ({
      items: [
        { title: 'About Click Motto' },
        { title: 'Pricing' },
        { title: 'License' },
        { title: 'Partnerships' },
        { title: 'Blog' },
        { title: 'Help' },
        { title: 'Join the Team' },
        
      ],
    }),
  }
</script>

<style scoped>
.navtext {
  font-style: normal !important;
}

</style>