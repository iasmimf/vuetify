<script setup>

defineProps({
  usuario: Object
  

});

</script>

<template>

   
    
      <tr>
        <td>{{ usuario.nome }}</td>

        <td>{{ usuario.data_nasc }}</td>

        <td>{{ usuario.email }}</td>
        
        <td>{{ usuario.whatsapp }}</td>
      </tr>
    
   
</template>