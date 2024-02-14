<script setup>

defineProps({
  cidade: Object,
  iasmime: String

});

</script>

<template>

    <v-col cols="12" sm="6" md="4" lg="3" >


        <v-card>  
        
        <v-img class="align-end text-white"
         :src="cidade.img">

         {{ iasmime }}
          
                  </v-img> 

                   <v-card-subtitle>
                    
                    {{ cidade.nome }}

                   </v-card-subtitle> 
                   
                   <v-card-text>

          População: {{ cidade.n_habitantes }}
                   </v-card-text>
                    

                   <v-card-text>
           Números de bairro: {{ cidade.n_bairros }}
                   </v-card-text>
                   <v-card-actions>
                    <v-btn variant="tonal" color="danger" >ver mais</v-btn>
                    <v-btn variant="tonal" color="success" >comprar</v-btn>
                    <v-btn icon="mdi-timer" variant="tonal" color="danger"></v-btn> 

                   </v-card-actions>

          </v-card> 


     </v-col>
</template>