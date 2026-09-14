<template>
    <v-container
    class="fill-height d-flex flex-column justify-center"
    max-width="1100">
      <div class="mb-8 text-center">
         <v-row>
          <v-col cols="12" md="4">
            <v-text-field v-model="firstName" label="First Name"></v-text-field>
          </v-col>

          <v-col cols="12" md="4">
            <v-text-field v-model="middleName" label="Middle Name"></v-text-field>
          </v-col>

          <v-col cols="12" md="4">
            <v-text-field v-model="lastName" label="Last Name"></v-text-field>
          </v-col>
        </v-row>
      </div>
      
      <div class="mb-8 text-center">
         <v-row>
          <v-col cols="12" md="4">
          <v-date-input v-model="birthDate" label="Birthdate"></v-date-input>
          </v-col>

          <v-col cols="12" md="4">
            <v-select v-model="civilStatus" label="Civil Status" :items="['Single', 'Maried', 'Widowed', 'Divorced', 'Separated']"></v-select>
          </v-col>

          <v-col cols="12" md="4">
            <v-select v-model="gender" label="Gender" :items="['Female', 'Male', 'Prefer not to say']"></v-select>
          </v-col>
        </v-row>  
      </div>

      <div class="mb-8 text-center">
         <v-row>
          <v-col cols="12" md="">
           <v-textarea clearable v-model="address" label="Address"></v-textarea>
          </v-col>
        </v-row> 
      </div>

      <div class="mb-8 text-center"> 
           <v-btn color="primary" density="default" @click="save">Save</v-btn>
            <v-btn color="warning" density="default"   @click="reset">Reset</v-btn>            
      </div>

      
    </v-container>
    

</template>

<script setup lang="ts">
import { ref } from 'vue'

const firstName = ref('')
const middleName = ref('')
const lastName = ref('')
const birthDate = ref('')
const civilStatus = ref('')
const gender= ref('')
const address = ref('')

function save(){
    console.log(firstName.value)
    console.log(middleName.value)
    console.log(lastName.value)
    console.log(birthDate.value)
    console.log(civilStatus.value)
    console.log(gender.value)
    console.log(address.value)
}

function reset(){
    firstName.value = ''
    middleName.value = ''
    lastName.value = ''
    birthDate.value = ''
    civilStatus.value = ''
    gender.value = ''
    address.value = ''    
}

</script>