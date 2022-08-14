<template>
<v-container fill-height align="center" justify="center">
<v-imge class="bg">
  <!-- :src="require('@/assets/sign/music.png')" -->
  <v-spacer />
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="4">
      <!-- <v-card elevation="8" class="mt-16 card py-6" >
      </v-card>  -->
        <v-spacer />      
        <v-autocomplete
      v-model="model"
      :items="items"
      :loading="isLoading"
      :search-input.sync="search"
      clearable
      rounded
      hide-details
      hide-selected
      item-text="name"
      item-value="symbol"
      label="Search..."
      solo
    >
    </v-autocomplete>
    </v-col>
  </v-row>

  <v-container
   
  >
    <v-fade-transition mode="out-in">
      <v-row>

        <v-col cols="6">
          <v-card>
            <v-img
              src="https://picsum.photos/350/165?random"
              max-height="125"
              class="grey darken-4"
            ></v-img>
            <v-card-title class="text-h6">
              ศูนย์บริการด้านสุขภาพจิตใกล้ตัว
            </v-card-title>
          </v-card>
        </v-col>


    <v-col cols="6">
          <v-card>
            <v-img
              src="https://picsum.photos/350/165?random"
              height="125"
              class="grey darken-4"
            ></v-img>
            <v-card-title class="text-h6">
              ปรึกษาแพทย์
            </v-card-title>
          </v-card>
        </v-col>

        <v-col cols="6">
          <v-card>
            <v-img
              src="https://picsum.photos/350/165?random"
              height="125"
              contain
              class="grey darken-4"
            ></v-img>
            <v-card-title class="text-h6">
              บทความให้กำลังใจ
            </v-card-title>
          </v-card>
        </v-col>

     

        <v-col cols="6">
          <v-card>
            <v-img
              src="https://picsum.photos/350/165?random"
              max-height="125"
              contain
              class="grey darken-4"
            ></v-img>
            <v-card-title class="text-h6">
                อบรมจิตวิทยา
            </v-card-title>
          </v-card>
        </v-col>
      </v-row>
    </v-fade-transition>
    <v-col class="mt-10 card py-2" align="center" justify="center">
    <v-btn rounded class="black--text" color="#A9A9A9" dark v-bind="attrs" v-on="on" @click="back()" >
                        กลับ
                    </v-btn></v-col>
  </v-container>
</v-imge>
</v-container>
</template>

<script>
import signinVue from './signin.vue'
export default {
  data() {
    return {
        dialog: false,
    }
  },
  created() {
    
  },
  methods: {
    back(){
      this.$router.back({name:'signin'})
    }
  },
}
</script>

<style scoped>
template {
    margin: auto;
    font-family: "Work Sans", sans-serif;
}

.logo {
    width: 60%;
    height: 60%;
}

.title {
    font-size: 16px;
    color: rgb(4, 4, 4);
}

.card {
    margin-left: 25%;
    width: 50%;
}

.btn {
    width: 100%;
}

#login {
    margin-top: 200px;
}

.bg {
    width: 100%;
    height: 100%;
    position: absolute;
    top: 0;
    left: 0;
    background: url('../assets/sign/mq.png');
    background-size: cover;
    transform: scale(1.17);
  }
</style>