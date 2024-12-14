<template>
  <v-sheet id="products" class="text-center py-16">
    <div class="text-h4 font-weight-bold">Our Products</div>

    <div class="text-body-1 text-medium-emphasis mt-5">
      Discover our wide range of products.
    </div>

    <v-container>
      <v-row class="mt-5 ga-7 pa-10" style="min-height: 700px">
        <v-col class="d-flex flex-column align-between ga-7">
          <v-row class="h-50 rounded">
            <v-col class="bg-grey-lighten-1">
              <v-card class="h-100 w-100 bg-grey-lighten-5 rounded">
              <v-card-title class="text-h6 text-center">THERMAL</v-card-title>
              <v-card-text class="bg-grey-lighten-5">
                <v-list lines="one" class="bg-grey-lighten-5">
                  <v-list-item v-for="(item, index) in Thermal" :key="index">
                    <v-list-item-title
                      class="text-decoration-none text-accent"
                    >
                      {{ item.item }}
                    </v-list-item-title>
                  </v-list-item>
                </v-list>
              </v-card-text>
            </v-card>
            </v-col>
           
          </v-row>

          <v-row class="h-50 bg-grey-lighten-1 rounded" >
            <v-col class="bg-grey-lighten-1">
              <v-card class="h-100 w-100 bg-grey-lighten-5 rounded">
              <v-card-title class="text-h6 text-center">POLYESTER</v-card-title>
              <v-card-text class="bg-grey-lighten-5">
                <v-list lines="one" class="bg-grey-lighten-5">
                  <v-list-item v-for="(item, index) in POLYESTER" :key="index">
                    <v-list-item-title
                      class="text-decoration-none text-accent"
                    >
                      {{ item.item }}
                    </v-list-item-title>
                  </v-list-item>
                </v-list>
              </v-card-text>
            </v-card>
            </v-col>
          
          </v-row>
        </v-col>

        <v-col class="bg-grey-lighten-1 rounded" >
          <v-card class="h-100 w-100 bg-grey-lighten-5 rounded">
              <v-card-title class="text-h6 text-center">BOPP</v-card-title>
              <v-card-text class="bg-grey-lighten-5">
                <v-list lines="one" class="bg-grey-lighten-5">
                  <v-list-item v-for="(item, index) in BOPP" :key="index">
                    <v-list-item-title
                      class="text-decoration-none text-accent"
                    >
                      {{ item.item }}
                    </v-list-item-title>
                  </v-list-item>
                </v-list>
              </v-card-text>
            </v-card>
        </v-col>

        <v-col class="d-flex flex-column align-between ga-7">
          <v-row class="h-25 bg-grey-lighten-1 rounded" >
            <v-col class="bg-grey-lighten-1 rounded" >
              <v-card class="h-100 w-100 bg-grey-lighten-5 rounded">
              <v-card-title class="text-h6 text-center">ASTRA  (LAMINATION)</v-card-title>
              <v-card-text class="bg-grey-lighten-5">
                <v-list lines="one" class="bg-grey-lighten-5">
                  <v-list-item v-for="(item, index) in ASTRA" :key="index">
                    <v-list-item
                      class="text-decoration-none text-accent"
                    >
                      {{ item.item }}
                    </v-list-item>
                  </v-list-item>
                </v-list>
              </v-card-text>
            </v-card>
            </v-col>
          </v-row>

          <v-row class="h-25 bg-grey-lighten-1 rounded" >
            <v-col class="bg-grey-lighten-1 rounded" >
              <v-card class="h-100 w-100 bg-grey-lighten-5 rounded">
              <v-card-title class="text-h6 text-center">ASTRA  (PASTING)</v-card-title>
              <v-card-text class="bg-grey-lighten-5">
                <v-list lines="one" class="bg-grey-lighten-5">
                  <v-list-item v-for="(item, index) in ASTRAP" :key="index">
                    <v-list-item
                      class="text-decoration-none text-accent"
                    >
                      {{ item.item }}
                    </v-list-item>
                  </v-list-item>
                </v-list>
              </v-card-text>
            </v-card>
            </v-col>
          </v-row>
          <v-row class="h-25 bg-grey-lighten-1 rounded" ><v-col class="bg-grey-lighten-1 rounded" >
              <v-card class="h-100 w-100 bg-grey-lighten-5 rounded">
              <v-card-title class="text-h6 text-center">HOLO (PASTING & LAMINATION)</v-card-title>
              <v-card-text class="bg-grey-lighten-5">
                <v-list lines="one" class="bg-grey-lighten-5">
                  <v-list-item v-for="(item, index) in HOLO" :key="index">
                    <v-list-item
                      class="text-decoration-none text-accent"
                    >
                      {{ item.item }}
                    </v-list-item>
                  </v-list-item>
                </v-list>
              </v-card-text>
            </v-card>
            </v-col></v-row>
          <v-row class="h-25 bg-grey-lighten-1 rounded" ><v-col class="bg-grey-lighten-1 rounded" >
              <v-card class="h-100 w-100 bg-grey-lighten-5 rounded">
              <v-card-title class="text-h6 text-center">ASTRA (UV, BOOK BINDING)</v-card-title>
              <v-card-text class="bg-grey-lighten-5">
                <v-list lines="one" class="bg-grey-lighten-5">
                  <v-list-item v-for="(item, index) in ASTRAB" :key="index">
                    <v-list-item
                      class="text-decoration-none text-accent"
                    >
                      {{ item.item }}
                    </v-list-item>
                  </v-list-item>
                </v-list>
              </v-card-text>
            </v-card>
            </v-col></v-row> 
        </v-col>
      </v-row>
    </v-container>
  </v-sheet>
</template>

<script setup>
import { ref } from "vue";

const dialog = ref(false);
const Thermal = [
  {
    item: "BOPP, PET GLOSS & MATT",
  },
  {
    item: "BOPP VELVET",
  },
  {
    item: "MET-PET GOLD GLOSS & MATT",
  },
   {
    item: "MET-PET SILVER GLOSS & MATT",
  },
  {
    item: "ANTI SCRATCH/SCUFF FREE",
  },
];
const POLYESTER = [
  {
    item: "CLEAR POLYESTER FILMS",
  },
  {
    item: "METALLISED POLYESTER FILMS",
  },
  {
    item: "PET MCUV (CC) - MET & CLEAR",
  },
   {
    item: "HOLLOGRAPHIC - MET & CLEAR",
  },
  {
    item: "THICK POLYESTER (WINDOW FILM)",
  },
];
const BOPP = [
  {
    item: "10 Micron Gloss",
  },
  {
    item: "12 Micron Gloss & MATT",
  },
  {
    item: "15 Micron Gloss & MATT",
  },
   {
    item: "8 Micron Gloss & Silver",
  },
  {
    item: "17 Micron Pearlise",
  },
  {
    item: "18 Micron Pearlise",
  },
  {
    item: "CLEAR HST BOPP",
  },
  {
    item: "MET HST BOPP",
  },
  {
    item: "21 Micron Velvet Soft-Touch",
  },
  {
    item: "Tape & Textile BOPP",
  },
  {
    item: "SELF ADHESIVE BOPP TAPE - TRN",
  },
  {
    item: "SELF ADHESIVE BOPP TAPE - BRN",
  },
  {
    item: "Opaque film",
  },
];
const ASTRA = [
  {
    item: "TC-177,TC-108,TC-107,TC-207,TC-101,TC-302 H,TC-511" },
];
const ASTRAP = [
  {
    item: "TC-777,TC-777H,TPW,TPW-100" },
];
const HOLO = [
  {
    item: "ANBOND-111, HOLO-USP, HOLO RG, HOLO-5051"
  }
]
const ASTRAB = [
  {
    item: "TMC-6322, TM-6046, TM-6060,TM-6077, TM-6099, ASCURE AC-402 D, ASCURE AC-651 RG, ASCURE AC - 655 RG, Turbolac 42 HRG, Excella-2000."
  }
]
</script>
