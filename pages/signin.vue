<template>
<v-container fill-height align="center" justify="center">
<v-imge class="bg">
  <!-- :src="require('@/assets/sign/music.png')" -->
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="6">
      <v-card elevation="8" class="mt-16 card py-6" >
        <v-card-text class="text-center" >
            <!-- <img class="logo" src="../assets/img/logomfu.png" /> -->
                
                <large>เข้าสู่ระบบ</large>

                
                <div class="col-12" />
                <v-text-field v-model="user" label="อีเมล" outlined></v-text-field>
                <v-text-field class="input-group--focused" :append-icon="eye ? 'mdi-eye' : 'mdi-eye-off'" :type="eye ? 'text' : 'password'" @click:append="eye = !eye" label="รหัสผ่าน" v-model="pass" outlined  ></v-text-field>
              
                <!-- <v-col sm="12" md="12">
                <v-btn class="ma-2" text icon color="indigo">
                <h4 justify="center" align="right"  >FORGOT YOUR PASSWORD?</h4>
                </v-btn>
                </v-col> -->
                <!-- <v-btn class="ma-2" text icon color="indigo"> -->
                <h4 justify="center" align="right"  >ลืมรหัสผ่าน?</h4>
                <div class="col-12" />
                

                <div class="text-center">
                    <v-btn rounded large class="black--text" color="#A9A9A9" dark v-bind="attrs" v-on="on" @click="next()" >
                        ตกลง

                    </v-btn>
                    <v-col sm="12" md="12">
                    <h4 justify="center" align="center" >OR</h4>
                    </v-col>
                   <v-btn width="50%" rounded large class="black--text" color="#FF0000" dark v-on:click="on()">
                       เหตุฉุกเฉิน
                    </v-btn>         
                </div>  
              
           
        </v-card-text>
      </v-card> 
    </v-col>
  </v-row>
</v-imge>
</v-container>
</template>

<script>
export default {
  data() {
    return {
      dialog: false,
      eye: false,
    }
  },
  computed: {
    },

    created() {
        this.initialize()
    },
  created() {
    
  },
  methods: {
     next(){
      this.$router.push({name:'home'})
    },
  },
}
</script>

<style scoped>
template {
    margin: auto;
    font-family: "Work Sans", sans-serif;
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