<template>
  <v-container>



    <div class="block galleryBlock">

      <v-toolbar flat class="gallerytab hidden-xs-only">
            <v-btn text>All</v-btn>
            <v-btn text>Photos</v-btn>
            <v-btn text>Videos</v-btn>
            <v-btn text>Freebies</v-btn>
            <v-btn text>360</v-btn>
          
          <v-spacer></v-spacer>

            <v-menu bottom left>
              <template v-slot:activator="{ on, attrs }">
                <v-btn
                
                  icon
                  v-bind="attrs"
                  v-on="on"
                >
                  <v-text style="margin-right: 100px;">Recommended</v-text>
                </v-btn>
              </template>

              <v-list class="dropclass2">
                <v-list-item
                  v-for="(item, i) in items"
                  :key="i"
                >
                  <v-list-item-title class="dropclassfont2">{{ item.title }}</v-list-item-title>
                </v-list-item>
              </v-list>
            </v-menu>

      </v-toolbar>


      <div class="hidden-sm-and-up">
        <v-menu offset-y>
          <template v-slot:activator="{ on }">
            <v-app-bar-nav-icon v-on="on"></v-app-bar-nav-icon>
          </template>
          <v-list class="responsiveMenu">
            <v-list-item>
              <v-list-item-title><router-link to="/">All</router-link></v-list-item-title>
            </v-list-item>
            <v-list-item>
              <v-list-item-title><router-link to="/">Photos</router-link></v-list-item-title>
            </v-list-item>
            <v-list-item>
              <v-list-item-title><router-link to="/">Vidoes</router-link></v-list-item-title>
            </v-list-item>
            <v-list-item>
              <v-list-item-title><router-link to="/">Freebies</router-link></v-list-item-title>
            </v-list-item>
            <v-list-item>
              <v-list-item-title><router-link to="/">360</router-link></v-list-item-title>
            </v-list-item>
            <v-list-item>
              <v-list-item-title><router-link to="/">Recommended</router-link></v-list-item-title>
            </v-list-item>

          </v-list>
        </v-menu>
      </div>


        <v-row class="mb-1">
          <v-col
            v-for="n in 3"
            :key="n"
            class="d-flex child-flex"
            cols="4"
          >
            <v-img
              :src="`https://picsum.photos/500/300?image=${n * 5 + 10}`"
              :lazy-src="`https://picsum.photos/10/6?image=${n * 5 + 10}`"
              
              class="grey lighten-2 img1"
            >
              <template v-slot:placeholder>
                <v-row
                  class=" ma-0"
                  align="center"
                  justify="center"
                >
                  <v-progress-circular
                    indeterminate
                    color="grey lighten-5"
                  ></v-progress-circular>
                </v-row>
              </template>
            </v-img>
          </v-col>
        </v-row>


      <v-row class="mb-2">
          <v-col
            v-for="n in 3"
            :key="n"
            class="d-flex child-flex"
            cols="4"
          >
            <v-img
              :src="`https://picsum.photos/200/300?image=${n * 6 + 10}`"
              :lazy-src="`https://picsum.photos/10/6?image=${n * 5 + 10}`"
              
              class="grey lighten-2 img1"
            >
              <template v-slot:placeholder>
                <v-row
                  class=" ma-0"
                  align="center"
                  justify="center"
                >
                  <v-progress-circular
                    indeterminate
                    color="grey lighten-5"
                  ></v-progress-circular>
                </v-row>
              </template>
            </v-img>
          </v-col>
        </v-row>

        <v-row class="mb-2">
          <v-col
            v-for="n in 3"
            :key="n"
            class="d-flex child-flex"
            cols="4"
          >
            <v-img
              :src="`https://picsum.photos/500/300?image=${n * 7 + 10}`"
              :lazy-src="`https://picsum.photos/10/6?image=${n * 5 + 10}`"
              
              class="grey lighten-2 img1"
            >
              <template v-slot:placeholder>
                <v-row
                  class=" ma-0"
                  align="center"
                  justify="center"
                >
                  <v-progress-circular
                    indeterminate
                    color="grey lighten-5"
                  ></v-progress-circular>
                </v-row>
              </template>
            </v-img>
          </v-col>
        </v-row>

        <v-row class="mb-2">
          <v-col
            v-for="n in 3"
            :key="n"
            class="d-flex child-flex"
            cols="4"
          >
            <v-img
              :src="`https://picsum.photos/300/300?image=${n * 8 + 10}`"
              :lazy-src="`https://picsum.photos/10/6?image=${n * 5 + 10}`"
              
              class="grey lighten-2 img1"
            >
              <template v-slot:placeholder>
                <v-row
                  class=" ma-0"
                  align="center"
                  justify="center"
                >
                  <v-progress-circular
                    indeterminate
                    color="grey lighten-5"
                  ></v-progress-circular>
                </v-row>
              </template>
            </v-img>
          </v-col>
        </v-row>

    </div>
    
  </v-container>

  
</template>

<script>
  export default {
    name: 'Gallery',

    data: () => ({
      items: [
        { title: 'Most Recent' },
        { title: 'Most Viewed' },
        { title: 'Most Downloaded' },
        { title: 'Most Appreciated' },
        
      ],
    }),
  }
</script>

<style scoped>

</style>