<script setup>

defineProps({
 bairros : Object
  

});

</script>

<template>

   
       <div v-for="bairro in bairros" >
          <h3>{{ bairro.nome_bairro }}</h3>
    

        </div>
</template>