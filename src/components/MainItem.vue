<template>
    <v-card
      class="mx-auto"
      max-width="448"
      color="red-lighten-2"
    >
    
      <v-layout min-height="800px">
        
        <!-- <v-app-bar
          density="compact"
        >
          <template v-slot:prepend>
            <v-app-bar-nav-icon variant="text" @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
          </template>
  
          <v-app-bar-title></v-app-bar-title>
  
          <template v-if="$vuetify.display.mdAndUp">
            <v-btn icon="mdi-magnify" variant="text"></v-btn>

            <v-btn icon="mdi-filter" variant="text"></v-btn>
            </template>

            <v-btn icon="mdi-dots-vertical" variant="text"></v-btn>
        </v-app-bar> -->
        <v-navigation-drawer
        v-model="drawer"
        :location="$vuetify.display.mobile ? 'bottom' : undefined"
        temporary
      >
        
        <v-list
          :items="items"
        ></v-list>
      </v-navigation-drawer>
       
        <v-main>
            <v-card min-height="80" class="rounded-xl my-2 mx-2"
            >
            <v-row>
                <v-col>
                    <v-card
                        color="red-lighten-2"                
                        variant="outlined"
                        class="rounded-xl my-2 mx-2"
                        height="70"
                    >
                    <v-card-item
                    prepend-avatar="https://randomuser.me/api/portraits/women/81.jpg"
                    title="Hello! Yem Daramony"            
                    >
                    
                    </v-card-item>
                    </v-card>
                </v-col>
            </v-row>
            
            
            </v-card>
            <v-card  class="rounded-xl mx-2">
                <v-container fluid>
                  <v-row dense>
                      <v-col cols="4">
                          <v-hover>
                          <template v-slot:default="{ isHovering, props }">
      
                          <v-card 
                            class="rounded-xl"
                            style="text-align: center;"
                              v-bind="props"
                              :color="isHovering ? colorTheme : colorTheme"
                              min-height="100" :variant="isHovering ? 'elevated' : 'outlined'" color="red-lighten-2">
                            <v-card-item>
                            <v-icon style="font-size: 50px;">
                                mdi-github
                            </v-icon>
                            <br>
                            Payment
                           </v-card-item>
                        </v-card>
                          </template>
                          </v-hover>
                      </v-col>
                      <v-col cols="4">
                          <v-hover>
                          <template v-slot:default="{ isHovering, props }">
      
                          <v-card 
                            class="rounded-xl"
                            style="text-align: center;"
                              v-bind="props"
                              :color="isHovering ? colorTheme : colorTheme"
                              min-height="100" :variant="isHovering ? 'elevated' : 'outlined'" 
                              >
                            <v-card-item>
                            <v-icon style="font-size: 50px;">
                                mdi-account-circle
                            </v-icon>
                            <br>
                            Account
                           </v-card-item>
                        </v-card>
                          </template>
                          </v-hover>
                      </v-col>
                      <v-col cols="4">
                          <v-hover>
                          <template v-slot:default="{ isHovering, props }">
      
                          <v-card 
                            class="rounded-xl"
                            style="text-align: center;"
                              v-bind="props"
                              :color="isHovering ? 'red-lighten-2' : 'red-lighten-2'"
                              min-height="100" :variant="isHovering ? 'elevated' : 'outlined'" color="red-lighten-2">
                            <v-card-item>
                            <v-icon style="font-size: 50px;">
                                mdi-mailbox
                            </v-icon>
                            <br>
                            Mail
                           </v-card-item>
                        </v-card>
                          </template>
                          </v-hover>
                      </v-col>
                      <v-col cols="4">
                          <v-hover>
                          <template v-slot:default="{ isHovering, props }">
      
                          <v-card 
                            class="rounded-xl"
                            style="text-align: center;"
                              v-bind="props"
                              :color="isHovering ? 'red-lighten-2' : 'red-lighten-2'"
                              min-height="100" :variant="isHovering ? 'elevated' : 'outlined'" color="red-lighten-2">
                            <v-card-item>
                            <v-icon style="font-size: 50px;">
                                mdi-wallet
                            </v-icon>
                            <br>
                            Wallet
                           </v-card-item>
                        </v-card>
                          </template>
                          </v-hover>
                      </v-col>
                      <v-col cols="4">
                          <v-hover>
                          <template v-slot:default="{ isHovering, props }">
      
                          <v-card 
                            class="rounded-xl"
                            style="text-align: center;"
                              v-bind="props"
                              :color="isHovering ? 'red-lighten-2' : 'red-lighten-2'"
                              min-height="100" :variant="isHovering ? 'elevated' : 'outlined'" color="red-lighten-2">
                            <v-card-item>
                            <v-icon style="font-size: 50px;">
                                mdi-chart-pie
                            </v-icon>
                            <br>
                            Static
                           </v-card-item>
                        </v-card>
                          </template>
                          </v-hover>
                      </v-col>
                      <v-col cols="4">
                          <v-hover>
                          <template v-slot:default="{ isHovering, props }">
      
                          <v-card 
                            class="rounded-xl"
                            style="text-align: center;"
                              v-bind="props"
                              :color="isHovering ? 'red-lighten-2' : 'red-lighten-2'"
                              min-height="100" :variant="isHovering ? 'elevated' : 'outlined'" color="red-lighten-2">
                            <v-card-item>
                            <v-icon style="font-size: 50px;">
                                mdi-chart-pie
                            </v-icon>
                            <br>
                            Static
                           </v-card-item>
                        </v-card>
                          </template>
                          </v-hover>
                      </v-col>
                      <v-col cols="4">
                          <v-hover>
                          <template v-slot:default="{ isHovering, props }">
      
                          <v-card 
                            class="rounded-xl"
                            style="text-align: center;"
                              v-bind="props"
                              :color="isHovering ? 'red-lighten-2' : 'red-lighten-2'"
                              min-height="100" :variant="isHovering ? 'elevated' : 'outlined'" color="red-lighten-2">
                            <v-card-item>
                            <v-icon style="font-size: 50px;">
                                mdi-chart-pie
                            </v-icon>
                            <br>
                            Static
                           </v-card-item>
                        </v-card>
                          </template>
                          </v-hover>
                      </v-col>
                      <v-col cols="4">
                          <v-hover>
                          <template v-slot:default="{ isHovering, props }">
      
                          <v-card 
                            class="rounded-xl"
                            style="text-align: center;"
                              v-bind="props"
                              :color="isHovering ? 'red-lighten-2' : 'red-lighten-2'"
                              min-height="100" :variant="isHovering ? 'elevated' : 'outlined'" color="red-lighten-2">
                            <v-card-item>
                            <v-icon style="font-size: 50px;">
                                mdi-chart-pie
                            </v-icon>
                            <br>
                            Static
                           </v-card-item>
                        </v-card>
                          </template>
                          </v-hover>
                      </v-col>
                      <v-col cols="4">
                          <v-hover>
                          <template v-slot:default="{ isHovering, props }">
      
                          <v-card 
                            class="rounded-xl"
                            style="text-align: center;"
                              v-bind="props"
                              :color="isHovering ? 'red-lighten-2' : 'red-lighten-2'"
                              min-height="100" :variant="isHovering ? 'elevated' : 'outlined'" color="red-lighten-2">
                            <v-card-item>
                            <v-icon style="font-size: 50px;">
                                mdi-chart-pie
                            </v-icon>
                            <br>
                            Static
                           </v-card-item>
                        </v-card>
                          </template>
                          </v-hover>
                      </v-col>
                  </v-row>
                </v-container>
            </v-card>
            <div class="mx-2 my-2">
                <b>Promotions & Events</b>
            </div>
            <v-card min-height="110" class="rounded-xl my-2 mx-2"
            >
            <v-row>
                <v-col>
                    <v-card
                        color="red-lighten-2"                
                        variant="outlined"
                        class="rounded-xl my-2 mx-2"
                        height="120"
                    >
                    <v-card-item
                    >
                    </v-card-item>
                        
                    </v-card>
                </v-col>
            </v-row>
            
            
            </v-card>

            <div class="mx-2">
                <b>Order Service</b>
            </div>
            <v-card min-height="110" class="rounded-xl my-2 mx-2"
            >
            <v-row>
                <v-col>
                    <v-card
                        :color="colorTheme"                
                        variant="outlined"
                        class="rounded-xl my-2 mx-2"
                        height="90"
                    >
                    <v-card-item
                    >
    
                    <v-card class="rounded-xl" height="70" width="70" :color="colorTheme">

                    </v-card>
                    </v-card-item>
                        
                    </v-card>
                </v-col>
            </v-row>
            
            
            </v-card>
        </v-main>
      </v-layout>
    </v-card>
  </template>

<script setup>
import { ref, watch } from 'vue';

const drawer = ref(false);
const group = ref(null);

var colorTheme = ref('red-lighten-2');
const items = ref([
    {
        title: 'Foo',
        value: 'foo',
    },
    {
        title: 'Bar',
        value: 'bar',
    },
    {
        title: 'Fizz',
        value: 'fizz',
    },
    {
        title: 'Buzz',
        value: 'buzz',
    },
]);
watch(group, () => {
  drawer.value = false
});
</script>

<style lang="scss" scoped>

</style>