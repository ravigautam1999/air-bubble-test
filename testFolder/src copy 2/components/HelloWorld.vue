<template>
  <div>
    <!-- <v-footer>
      <v-row>
        <v-col v-for="(r,indx) in list" :key="indx">
          <span v-if="indx%2 === 0">
            { "country": "{{ r }}",
          </span>
          <span v-else>
            "currency": "{{ r }}" },
          </span>
        </v-col>
      </v-row>
    </v-footer> -->
    <v-row
    align="center"
    justify="center"
  >
    <v-card
    >
      <v-row justify="center">
        <v-btn
          color="success"
          class="mt-12"
          @click="overlay = !overlay"
        >
          Show Overlay
        </v-btn>

        <v-overlay
          :absolute="absolute"
          :value="overlay"
        >
          <v-btn
            color="success"
            @click="overlay = false"
          >
            Hide Overlay
          </v-btn>
        </v-overlay>
      </v-row>
    </v-card>
  </v-row>

  </div>
</template>

<script setup>
import {ref} from "vue";
import list from "../assets/dummyData/footerTabsItems.json";

const absolute =ref( true)
const overlay =ref(false)
</script>
