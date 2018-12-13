<template>
  <q-page class="flex flex-center">
      <q-btn color="primary" class="full-width">
       <label>
        {{scenes.all[0].name}}
          </label>
        </q-btn>
      <q-btn color="primary" class="full-width" label="Full-width" />
     <!--<div>Choose your dream</div> -->
       </q-page>
</template>

<script>
import scenes from '../data/recordings';

export default {
      name: 'PageMenu',
    data(){
        return {
        scenes,
        };
    },


};

</script>