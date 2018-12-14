<template>
  <q-page class="flex flex-center">
    <h2>{{this.$route.params.id}}</h2>
     <div>Cosmic Voyage Dreaming</div>
    <vue-audio :file ="file1"  />
    <img alt="Quasar logo" src="~assets/sleep.png">
   
  </q-page>
</template>

<style>
</style>

<script>
import VueAudio from 'vue-audio';
import VuetifyAudio from 'vuetify-audio';

export default {
  name: 'Index',
data() {
  return {
    //file1: '../assets/theJoker.mp3'
   // file1: 'http://localhost:3003/music?id=CosmicVoyageDreaming.mp3'
   file1: 'http://ec2-54-213-9-36.us-west-2.compute.amazonaws.com:3003/music?id=CosmicVoyageDreaming.mp3'

   //file1: 'statics//CosmicVoyageDreaming.mp3'
  };

},
components: {
  'vue-audio': VueAudio,
  'vuetify-audio': VuetifyAudio
},
methods:{
playSound() {
  console.log('About to play audio');
var audio = new Audio('../assets/theJoker.mp3');
      //  audio.play();

},
 audioFinish () {
            console.log('You see this means audio finish.');
        }
},
mounted : function(){
  this.playSound();
}
}
</script>
