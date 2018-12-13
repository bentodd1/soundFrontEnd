<template>

  <q-page class="flex flex-center">
    <q-item v-for="recording in recordings.all" >
      <q-btn color="primary" class="full-width">
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

export default {
      name: 'PageMenu',
    data(){
        return {
        recordings,
        };
    },


};

</script>