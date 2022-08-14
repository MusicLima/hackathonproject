<template>
<v-container fill-height align="center" justify="center">
<v-imge class="bg">
  <!-- :src="require('@/assets/sign/music.png')" -->
  <v-spacer />
  <v-row >
    <!-- <h1>Welcome to</h1> -->
    <v-spacer />
    <v-col class="mt-16 card py-2" align="center" justify="center">
      <v-row >
       
                    <v-btn rounded large class="black--text" color="#A9A9A9" dark v-bind="attrs" v-on="on" @click="next()" >
                    
                        เข้าสู่เว็บไซต์
                    </v-btn>
                       <!-- <button class="black--text" color="#A9A9A9" @click="next()">เข้าสู่เว็บไซต์</button> -->
      </v-row>
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
    }
  },
  created() {
    
  },
  methods: {
    next() {
      this.$router.push({ name: "signin" });
    },
    back() {
      this.$router.back();
    },
  },
}
</script>

<style scoped>
template {
    margin: auto;
    font-family: "Work Sans", sans-serif;
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