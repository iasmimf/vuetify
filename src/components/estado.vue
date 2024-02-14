<script setup>
import cidade from '@/components/cidade.vue';

defineProps({
 estados : Object
  

});

</script>

<template>

   
       <div v-for="estado in estados" >
          <h2>{{ estado.nome_estado }}</h2>
     
          <cidade :cidades="estado.cidades" />

        </div>
</template>