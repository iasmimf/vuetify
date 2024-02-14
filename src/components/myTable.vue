<script setup>

defineProps({
  items: Array
});

</script>

<template>

   
<v-card flat class="border mb-4">
  <v-table>
    <thead>
      <tr>
        <th>Nome</th>
        <th>Data de nacimento</th>
        <th>Email</th>
        <th>Whatsapp</th>
      </tr>
    </thead>
  <tbody>

   
 
    
    
    <tr v-for="item in items" >

        <td>{{ item.nome }}</td>

        <td>{{ item.data_nasc }}</td>

        <td>{{ item.email }}</td>
        
        <td>{{ item.whatsapp }}</td>
      </tr>

  </tbody>


  </v-table>
</v-card>
    
   
</template>