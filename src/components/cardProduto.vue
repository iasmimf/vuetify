<script setup>

defineProps({
  produto: Object
 

});

</script>

<template>

    <v-col cols="12" sm="6" md="4" lg="3" >


        <v-card>  
        
        <v-img :src="produto.img">

         
          
                  </v-img> 

                   <v-card-subtitle>
                    
                    {{ produto.nome }}

                   </v-card-subtitle> 
                   
                   <v-card-text v-for="tamanho in produto.tamanhos">
                        

              pequeno: {{tamanho.p}} <br>


              medio: {{tamanho.m}} <br>

              grande: {{tamanho.g}} <br>

                   </v-card-text>
                    

                   <v-card-text>
                 {{ produto.quant}}
                   </v-card-text>








                   <v-card-actions>
                    <v-btn variant="tonal" color="danger" >ver mais</v-btn>
                    <v-btn variant="tonal" color="success" >comprar</v-btn>
                    <v-btn icon="mdi-timer" variant="tonal" color="danger"></v-btn> 

                   </v-card-actions>

          </v-card> 


     </v-col>
</template>