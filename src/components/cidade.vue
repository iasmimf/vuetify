<script setup>
import bairro from '@/components/bairro.vue';

defineProps({
 cidades : Object
  

});

</script>

<template>

   
       <div v-for="cidade in cidades" >
          <h3>{{ cidade.nome_cidade }}</h3>
        
         <bairro :bairros="cidade.bairros" />

        </div>
</template>