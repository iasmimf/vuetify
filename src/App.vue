 <script setup>

  import HelloWorld from '@/components/HelloWorld.vue';
  import MeuCoponets from '@/components/MeuCoponets.vue';
  import minha_Tabela from '@/components/minha_Tabela.vue';
  import myTable from '@/components/myTable.vue';
  import estado from '@/components/estado.vue';
  
   import { ref } from 'vue';

    const isDrawerOpen = ref(false);
    const isDialogOpen = ref(false);
    const emailRules = [
  value => {
    if (value) return true;

      return'o email é obrigatório';
  }, 
    value =>{
      if (value.includes( '@'))return true; 
      return 'email invalido'
    }
];
    const nameRules = [
      value=> {
      if (value) return true;
      return 'o nome é obrigatorio';
     },
     value => {
      if (value.includes('linda')) return true;
      return 'nome invalido'
     }
    ] ;
    const cargoRules = [
      value=> {
      if (value) return true;
      return 'o cargo é obrigatorio';
     },
   
    ] ;

    const myArray = ['luciano', 'veronica', 'iasmim', 'tontom', 'mirian', 'dodo','luciano'];
    
    const arrayCidades = [
      { 'nome':'Curitiba', 'n_habitantes': 1700000, 'n_bairros':12, 'img': 'https://images.pexels.com/photos/18466185/pexels-photo-18466185/free-photo-of-jardim-botanico-brasil-construcao-predio.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1'},
      { 'nome':'Santos', 'n_habitantes': 500000, 'n_bairros':7, 'img': 'https://images.pexels.com/photos/19748912/pexels-photo-19748912/free-photo-of-nascer-do-sol-no-mar.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1'},
      { 'nome':'São Paulo', 'n_habitantes': 15100000, 'n_bairros':37, 'img': 'https://images.pexels.com/photos/3044565/pexels-photo-3044565.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1'},
      { 'nome':'Brasilia', 'n_habitantes': 4000, 'n_bairros':15, 'img': 'https://images.pexels.com/photos/17007873/pexels-photo-17007873/free-photo-of-brasil-catolicismo-igreja-capela.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1'},

    ];
    const usuarios = 
[
{ "nome": "Luciano", "data_nasc" : "09/09/09/1982" , "email" : "luciano@luve.com.br", "whatsapp" : "41 98794-4067" },
{ "nome": "Veronica", "data_nasc" : "09/11/09/1984" , "email" : "veronica@luve.com.br", "whatsapp" : "41 98794-3889" },
{ "nome": "Iasmim", "data_nasc" : "06/06/2013" , "email" : "iasmimferenczuk@gmail.com", "whatsapp" : "41 98794-0000" },
{ "nome": "Adriana", "data_nasc" : "12/03/1984" , "email" : "suporte@contabilit.com.br", "whatsapp" : "13 99115-4530" },
{ "nome": "Mirian", "data_nasc" : "10/05/1967" , "email" : "mirian@gmail.com", "whatsapp" : "13 97840-8999" },
{ "nome": "Rafael", "data_nasc" : "18/10/1973" , "email" : "marcos@gmail.com", "whatsapp" : "11 98563-5249" },
{ "nome": "Antonio", "data_nasc" : "23/03/1954" , "email" : "antonio@gmail.com", "whatsapp" : "13 99140-3330" }
];
const produtos = [
      { 'nome':'calça leg', 'quant':1248, 'tamanhos': [{'p':416, 'm':416 , 'g':416 }] , 'img': 'https://images.pexels.com/photos/18466185/pexels-photo-18466185/free-photo-of-jardim-botanico-brasil-construcao-predio.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1'},
      { 'nome':'moletom', 'quant': 7554, 'tamanhos': [{'p':2518, 'm':2518, 'g':2518 }] , 'img': 'https://images.pexels.com/photos/19748912/pexels-photo-19748912/free-photo-of-nascer-do-sol-no-mar.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1'},
      { 'nome':'tenis', 'quant': 3333, 'tamanhos': [{'p':1111, 'm':1111 , 'g':1111 }] , 'img': 'https://images.pexels.com/photos/3044565/pexels-photo-3044565.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1'},
      { 'nome':'sandalia', 'quant': 6666, 'tamanhos': [{'p':2222, 'm':2222 , 'g':2222 }] , 'img': 'https://images.pexels.com/photos/17007873/pexels-photo-17007873/free-photo-of-brasil-catolicismo-igreja-capela.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1'},

    ];

    const paises = [

      {'nome_pais':'Brasil', 
          'estados':[
              {'nome_estado':'Paraná',

                'cidades': [

                    {'nome_cidade':'Curitiba', 

                        'bairros': [
                            {'nome_bairro':'Barrerinha'},
                            {'nome_bairro':'Batel'},
                           
                         ]
                    },

                    {'nome_cidade':'Almirante Tamandaré', 
                        'bairros': [
                            {'nome_bairro':'Cachoeira'},
                            {'nome_bairro':'Botiatuba'},
                          
                          ]
                        
                    },

                        
                  ]
              },

            
              {'nome_estado':'São Paulo',
              
                'cidades': [

                    {'nome_cidade':'São vicente', 

                        'bairros': [
                            {'nome_bairro':'Jokei Club'},
                            {'nome_bairro':'Vila Matias'},
                           
                         ]
                    },
 
                    {'nome_cidade':'Praia Grande', 
                        'bairros': [
                            {'nome_bairro':'Canto do Forte'},
                            {'nome_bairro':'Quietude'},
                          
                          ]
                        
                    },

                        
                  ]
              },

            ]

    },
//////////////////////////////////////////////////////////////////////////


{'nome_pais':'Estados Unidos', 
          'estados':[
              {'nome_estado':'Georgia',

                'cidades': [

                    {'nome_cidade':'Atlanta', 

                        'bairros': [
                            {'nome_bairro':'Midtown'},
                            {'nome_bairro':'Virginia Highland.'},
                           
                         ]
                    },

                    {'nome_cidade':'Columbus', 
                        'bairros': [
                            {'nome_bairro':'German Village'},
                            {'nome_bairro':'Victorian Village'},
                          
                          ]
                        
                    },

                        
                  ]
              },

        
              {'nome_estado':'nova york',
              
                'cidades': [

                    {'nome_cidade':' Manhattan', 

                        'bairros': [
                            {'nome_bairro':'East Village'},
                            {'nome_bairro':'Greenwich Village'},
                           
                         ]
                    },

                    {'nome_cidade':'Brooklyn', 
                        'bairros': [
                            {'nome_bairro':'Greenpoint.'},
                            {'nome_bairro':'Park Slope'},
                          
                          ]
                        
                    },

                        
                  ]
              },

            ]

    },



    ]; 
     
 

 </script> 

 <template>
  <v-app>
   
    <v-navigation-drawer v-model="isDrawerOpen">

    <v-list>
    <v-list-subheader>menu</v-list-subheader>
    <v-list-item prepend-icon="mdi-home">home</v-list-item>
    <v-list-item prepend-icon="mdi-account">usuário</v-list-item>
    <v-list-group>

      <template v-slot:activator="{ props }">
          <v-list-item
            v-bind="props"
            prepend-icon="mdi-account" 
            title="Cliente">
            
          </v-list-item>
        </template>

        <v-list-item prepend-icon="mdi-currency-usd">vendas</v-list-item>
        <v-list-item prepend-icon="mdi-chart-areaspline">relatorio</v-list-item>


    </v-list-group>
    </v-list>
    
    
    
    
    </v-navigation-drawer>
     
     <v-app-bar flat class="border-b">

      <v-app-bar-nav-icon @click="isDrawerOpen = !isDrawerOpen" ></v-app-bar-nav-icon>

       <v-app-bar-title>meu app</v-app-bar-title>
      
      
      
      
      
  
         
       <template #append>

      <v-menu>
        <template #activator="{props}"> 


       <v-btn icon class="mr-2"> 
        
        <v-badge dot color="amber"> 

         <v-icon icon="mdi-bell"></v-icon> 

           </v-badge>

       </v-btn>

      </template>
      <v-card min-width="200px" >
        <v-list>
         <v-list-item prepend-icon="alert-circle">
           <v-list-item-title>
            é importante
           </v-list-item-title>
         </v-list-item >


         


        </v-list>
      </v-card> 
    </v-menu> 

       </template>

        <v-menu>

          <template > 

         <v-avatar v-bind="props">
          
            <v-img cover src="/avatar.png"></v-img>
        
         </v-avatar>

        </template>

      <v-card min-width="200px">
        <v-list :lines="false" density="compact" nav>
          <v-list-item prepend-icon="mdi-account" >
              <v-list-item-title>
                meu pefil
              </v-list-item-title>
          </v-list-item>
     

        
          <v-list-item prepend-icon="mdi-heart">
              <v-list-item-title>
                favoritos
              </v-list-item-title>
          </v-list-item>
        </v-list>
      </v-card>

      
        </v-menu>   
        
          

      </v-app-bar>
    <v-main>
      <v-container> 
        <br><br><br>
        
        
        <div v-for="pais in paises">
        <h1>{{ pais.nome_pais }}</h1>



        <estado :estados="pais.estados"/>


        </div>
        
        
        
        
        
        <br><br><br><br><br><br><br><br><br>



         <pre> 
         {{ paises }}
        </pre>   
     



<br><br><br><br><br><br><br><br><br><br><br><br>

























        <v-btn color="secondary">teste theme</v-btn>




       <h1>dashboard</h1>

    <v-card flat class="border mb-4">
    <div class="d-flex justify-space-between">
       <v-card-title>ultimos usuarios</v-card-title>


       <v-card-title>
           <v-btn @click="isDialogOpen = true" variant="tonal" size="small">adionar usuarios</v-btn>
         
           <v-dialog v-model="isDialogOpen" width="500px">
   
   
               <v-card>
                <v-card-text>
                  <v-row>
                    <v-col>
                      <v-text-field 
                      label="Nome"
                      :rules="nameRules"
                      ></v-text-field>
                    </v-col>

                    <v-col>
                      <v-text-field
                       label="Email"
                        :rules="emailRules"     >
                      </v-text-field>
                    </v-col>

                  </v-row>
                      <v-select
                      label="cargo"
                      :items="['admin','gerente','convidado']"
                      :rules="cargoRules"
                      ></v-select>
                    
                </v-card-text>
                <v-card-actions>
                  <v-spacer></v-spacer>
                  <v-btn variant="text" @click="isDialogOpen = false">cancelar</v-btn>
                  <v-btn variant="tonal" color="success">salvar</v-btn>
                </v-card-actions>

               </v-card>
          </v-dialog> 
      
       </v-card-title>
    </div>
     
                  
           


 
    
      <v-table>
        <thead>
          <tr>
            <th>nome</th>
            <th>email</th>
            <th>cargo</th>
            <th>ações</th>
           
          </tr>
        </thead>
          <tbody>
          <tr>
            <td>jurema</td>
            <td>jurema@legal.luve</td>
            <td>
              <v-chip color="primary" variant="outlined" size="small"  >admin</v-chip>
            </td>
            <td>
              <v-btn prepend-icon="mdi-pencil " variant="tonal" color="success" :ripple="true" >editar</v-btn>
            </td>
          </tr>
          <tr>
            <td>jubscrelda</td>
            <td>jubscrelda.com.br</td>
            <td>  
              <v-chip color="success" variant="outlined" size="small">gerente</v-chip>
            </td>
            <td><v-btn prepend-icon="mdi-pencil" variant="tonal" color="success">editar</v-btn></td>
          </tr>
          <tr>
            <td>jubsvalda</td>
            <td>jubsvalda@do_santos.google</td>
            <td>
              <v-chip   variant="outlined" size="small">convidado</v-chip>
            </td>
           <td><v-btn prepend-icon="mdi-pencil" variant="tonal" color="success">editar</v-btn></td> 
          </tr>
          </tbody>
      </v-table>
  </v-card>

   





  <v-row>

    <cardProduto v-for="produto in produtos"  :produto="produto" />

  </v-row>












Desafio Iasmim
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

    <minha_Tabela v-for="usuario in usuarios" :usuario="usuario" />

  </tbody>


  </v-table>
</v-card>
   <hr> 


Outra Forma de Fazer

<myTable :items="usuarios" />


  <pre>
    {{ arrayCidades }}
  </pre>


  <hr>

  <div v-for="cidade in arrayCidades">

    <h2>{{ cidade.nome }}</h2>
    <p>Nº Hab: {{ cidade.n_habitantes }}</p>
    <p>Nº bairros: {{ cidade.n_bairros }}</p>
   <v-btn>visitar</v-btn>
   

  </div>
        
    <v-row>
      <MeuCoponets v-for="cidade in arrayCidades" :cidade="cidade" iasmime="Linda"/>

    



    </v-row>

  </v-container>
  </v-main>
</v-app>
<hr> <h3>Trabalhando com Arrays</h3>

{{ myArray }}<hr>



  
  <h2 v-for="nome in myArray" variant="tonal" size="small">{{ nome }}</h2>


  
         
 <hr>
<HelloWorld />
</template>
    
    
 


