<template>
  <v-sheet id="applications" class="py-16" color="secondary">
    <v-container>
      <v-row align="center">
        <v-col cols="12" md="6">
          <div class="text-h4 font-weight-medium">Applications for Every Need</div>

          <div class="text-body-1 text-medium-emphasis mt-5">
          Explore versatile and high-quality solutions tailored to meet diverse industry requirements. Whether it's packaging, publishing, or specialized films, we’ve got you covered.
          </div>

          <!-- <v-row class="mt-5"> -->
            <!-- <div v-for="(item, index) in ['TrustPilot', 'Feefo']" :key="item">
              <v-alert
                :border="index === 1 ? 'start' : undefined"
                class="pt-3 rounded-0"
                color="secondary"
              >
                <div class="font-weight-bold">
                  {{ item }}
                </div> -->

                <!-- <div>
                  <v-rating
                    color="yellow-darken-2"
                    density="compact"
                    model-value="5"
                  />
                </div> -->
              <!-- </v-alert> -->
            <!-- </div> -->
          <!-- </v-row> -->
        </v-col>

        <v-col cols="12" md="6">
          <v-alert
            v-for="(item, index) in applicationItems"
            :key="index"
            border="start"
            border-color="accent"
            class="my-5 border-opacity-100"
            color="white"
            elevation="5"
            rounded
          >
            <div class="d-flex flex-row align-center">
             
              <a
                :href="item.href"
                class="text-decoration-none text-accent font-weight-bold ml-2"
                :aria-label="item.ariaLabel"
              >
                {{ item.label }}
              </a>
            </div>
          </v-alert>
        </v-col>
      </v-row>
    </v-container>
  </v-sheet>
</template>

<script>
export default {
  data() {
    return {
      applicationItems: [
        {
          href: "#work",
          label: "Print Lamination",
        },
        {
          href: "#work",
          label: "Flexible Packaging",
        },
        {
          href: "#work",
          label: "Book Binding & Publishing",
        },
        {
          href: "#work",
          label: "Carton Window Films",
        },
        {
          href: "#work",
          label: "Food & Beverage Packaging",
        },
      ],
    };
  },
};
</script>
