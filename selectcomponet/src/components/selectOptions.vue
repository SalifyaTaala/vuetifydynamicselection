<template>
    <div id="SelectOptions">
      <v-container>
        <v-card>
            <v-card-title class="cool white--text">
                 <span class="headline">Fetching text-field Values Dynamically </span>
            </v-card-title>
            <v-divider></v-divider>
            <v-card-text>
                <v-row>
                    <v-col cols="12" sm="6" md="4">
                     <v-select  outlined v-model="selectedItem" :items="items" label="Country"></v-select>
                    </v-col>
           <v-col cols="12" sm="3" md="3">
             <v-text-field outlined v-model="capitalCity" label="Capital City"></v-text-field>

                    </v-col>
                     <v-col cols="12" sm="3" md="3">
             <v-text-field outlined v-model="nationalityDisplay" label="Nationality"></v-text-field>

                    </v-col>
                </v-row>
            </v-card-text>
        </v-card>
      </v-container>
    </div>
</template>
<script lang="ts">
import { Vue, Component } from "vue-property-decorator";
@Component({
    components: { }})
export default class SelectOptions extends Vue{
     private  selectedItem: string = "";
    private  items: any = [{
           text: "Nigeria",
           text2: "Abuja",
           text3: "Nigerian",
           value: 1
         },
          {
           text: "Ghana",
           text2: "Accra",
           text3: "Ghanain",
           value:2
         },
         {
           text: "Ethiopia",
           text2: "Addis Ababa",
           text3: "Ethiopian",
           value:3
         },
         {
           text: "Algeria",
           text2: "Algiers",
           text3: "Algerian",
           value:4
         },
         {
           text: "Eritrea",
           text2: "Asmara",
           text3: "Eritrean",
           value:5
         }
         ,
         {
           text: "Zambia",
           text2: "Lusaka",
           text3: "Zambian",
           value:6
         },
         {
           text: "Malawi",
           text2: "Lilongwe",
           text3: "Malawian",
           value:7
         }, {
           text: "Rwanda",
           text2: "Kigali",
           text3: "Rwandan",
           value:8
         },
          {
           text: "Tanzania",
           text2: "Dodoma",
           text3: "Tanzanian",
           value:9
         },
          {
           text: "Kenya",
           text2: "Nairobi",
           text3: "Kenyan",
           value:10
         },
          {
           text: "Guinea",
           text2: "Conakry",
           text3: "Guinean",
           value:11
         }, {
           text: "Uganda",
           text2: "Kampala",
           text3: "Ugandan",
           value:12
         },
       ]
    get  selectedCountry() {
       return this.items.find(item => item.value == this.selectedItem);
     }
    //  selected = this.selectedItem();
     get capitalCity() {

        return this.selectedCountry ? 
       this.selectedCountry.text2 : '';
   
    
     }
   
get nationalityDisplay(){
       return this.selectedCountry ? 
       this.selectedCountry.text3 : '';
}

   
 
    
}
</script>
<style scoped>
.cool{
  background-color: #212121 !important;
}
</style>