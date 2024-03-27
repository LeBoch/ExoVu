
<template>
 
  <!-- <div v-for="n in userLength">  
  <HumanEditor :userLength="userLength ">
 </HumanEditor>
  </div> -->
 
   <div>
     <div v-for="value in listUser" :key="value">
      {{ value.name }}  {{ value.firstname }}  {{ value.age }}
      <HumanEditor :name="value.name" :firstName="value.firstname" :age="value.age" @emitName="value.name = $event" @emitFirstName="value.firstname = $event" @emitAge="value.age = $event" ></HumanEditor>
     </div>
   </div>
 </template>
 
 <script setup>
 import HumanEditor from './components/HumanEditor.vue'
 import {reactive , ref} from "vue"
 const listUser = reactive([
   { "name": "Dupont", "firstname": "Jean", "age": 45 },
   { "name": "Martin", "firstname": "Pierre", "age": 30 },
   { "name": "Lefevre", "firstname": "Julie", "age": 25 },
   { "name": "Lemoine", "firstname": "Sophie", "age": 35 },
   { "name": "Moreau", "firstname": "Lucas", "age": 20 },
   { "name": "Simon", "firstname": "Paul", "age": 50 },
   { "name": "Laurent", "firstname": "Marie", "age": 40 },
   { "name": "Leroy", "firstname": "Camille", "age": 33 },
   { "name": "Roux", "firstname": "Alexandre", "age": 29 },
   { "name": "Bertrand", "firstname": "Nicolas", "age": 39 },
   { "name": "Girard", "firstname": "Charlotte", "age": 22 },
   { "name": "Lambert", "firstname": "Thomas", "age": 44 },
   { "name": "Rousseau", "firstname": "Maxime", "age": 31 },
   { "name": "Clement", "firstname": "Chloe", "age": 28 },
   { "name": "Lefebvre", "firstname": "Mathilde", "age": 37 },
   { "name": "Dumas", "firstname": "Quentin", "age": 41 },
   { "name": "Blanc", "firstname": "Justine", "age": 36 },
   { "name": "Guerin", "firstname": "Clément", "age": 32 },
   { "name": "Morin", "firstname": "Adrien", "age": 38 },
   { "name": "Gauthier", "firstname": "Maëlle", "age": 34 },
   { "name": "Perrin", "firstname": "Amandine", "age": 27 },
   { "name": "Chevalier", "firstname": "Théo", "age": 46 },
   { "name": "Francois", "firstname": "Valentin", "age": 43 },
   { "name": "Legrand", "firstname": "Axel", "age": 47 },
   { "name": "Gautier", "firstname": "Léa", "age": 23 },
   { "name": "Marchand", "firstname": "Anaïs", "age": 26 },
   { "name": "Marie", "firstname": "Lola", "age": 24 },
   { "name": "Dubois", "firstname": "Benoît", "age": 42 },
   { "name": "Dufour", "firstname": "Antoine", "age": 48 },
   { "name": "David", "firstname": "Alexis", "age": 49 }
 ]);
 const userLength = ref(listUser.length)
 
 </script>
 