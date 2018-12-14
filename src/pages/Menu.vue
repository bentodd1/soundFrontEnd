<template>

  <q-page class="flex flex-center">
    <q-item v-for="recording in recordings.all" >
      <q-btn color="primary" class="full-width" @click="goToDetail(recording.id)" >
       <label>
        {{recording.name}}
          </label>

        </q-btn>

     <!--<div>Choose your dream</div> -->
      </q-item>
       </q-page>

</template>

<script>
import recordings from '../data/recordings';
import Index from './index';

export default {
      name: 'PageMenu',
    data(){
        return {
        recordings,
        };
    },
     components: {
    Index,
 },
 methods: {
   goToDetail(id) {
    this.$router.push({name:'Index',params:{id:id}})
  }
 }


};

</script>