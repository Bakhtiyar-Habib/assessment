<template>
  <v-container>
    <div class="staticHero">
      <v-img :aspect-ratio="16/6" src="https://images.pexels.com/photos/1287124/pexels-photo-1287124.jpeg?auto=compress&cs=tinysrgb&dpr=3&h=750&w=1260">
        
        <v-row align="end" class="lightbox white--text pa-2">
          <v-col>
            <v-container class=" text-center">
              <div class="title">Your local source of high quality images and videos directly from their creators</div>
              <v-toolbar
                dark
                color="white"
                class="searchbox"
              >
                <v-toolbar-title class="search-title">Search Photos and Videos</v-toolbar-title>
                <v-spacer></v-spacer>
                <v-btn>
                  <v-icon>mdi-magnify</v-icon>
                </v-btn>
              </v-toolbar>
            </v-container>
            <small class="caption1"><b>Recommended:</b> summer, food, real estate, covid-19</small>
          </v-col>
        </v-row>
      </v-img>
    </div>


    <div class="category container">
      <h3>Top Categories</h3>


          <v-tabs
            background-color="white"
            show-arrows
            class="container"
          >

            <v-tab v-for="i in 15" :key="i" :href="'#tab-' + i" class="container">
              <v-img style="height: 175px; width: 20px;" :aspect-ratio="16/9" src="https://images.pexels.com/photos/2422461/pexels-photo-2422461.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940">
              </v-img>
            </v-tab>
          </v-tabs>

    </div>
    
  </v-container>
</template>

<script>
  export default {
    name: 'Hero',

    data: () => ({
      
    }),
  }
</script>

<style scoped>



</style>
