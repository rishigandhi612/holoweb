<template>
  <v-sheet id="home" class="mb-n4">
    <v-row>
      <!-- Text content column -->
      <v-col  cols="12" md="5" sm="12">
        <div style="min-height: 100px"></div>
        <v-container>
          <v-row class="mx-5 d-flex justify-end align-end text-end">
            <div class="text-h6 font-weight-light">
              HEMANT TRADERS COMPLETE POST PRESS SOLUTIONS | INDIA
            </div>
            <div class="text-h3 my-5">
              Speak to India's Leading Film & Adhesives Supplier.
            </div>
            <div class="text-h6 font-weight-light paragraph">
              We are Hemant Traders, a leading BOPP and Polyester (PET) film
              converters, Lamination and Book Binding Adhesives, UV
              Coat Suppliers based in Pune, MH, India. We offer an unrivalled
              level of service and a wide range of films, adhesives, and UV
              Coats for all applications.
            </div>
            <v-col cols="12">
              <v-btn
                variant="tonal"
                color="primary"
                class="mx-5"
                rounded
                size="large"
                href="tel:919422080922"
                target="_blank"
              >
                <v-icon class="mr-2">mdi-phone</v-icon>
                +91-9422080922
              </v-btn>

              <v-btn
                color="primary"
                elevation="0"
                variant="outlined"
                href="https://wa.me/919422080922"
                target="_blank"
                rounded
                size="large"
              >
                <v-icon>mdi-whatsapp</v-icon>
                WHATSAPP
              </v-btn>
            </v-col>
          </v-row>
        </v-container>
      </v-col>

      <!-- SVG content column -->
      <v-col md="7" class="hidden-sm-and-down">
        <svg
          id="visual"
          viewBox="0 0 900 600"
          width="900"
          height="600"
          xmlns="http://www.w3.org/2000/svg"
          xmlns:xlink="http://www.w3.org/1999/xlink"
          version="1.1"
        >
          <rect x="0" y="0" width="900" height="600" fill="#FFFFFF"></rect>
          <path
            d="M649 600L594.3 583.3C539.7 566.7 430.3 533.3 352 500C273.7 466.7 226.3 433.3 229.8 400C233.3 366.7 287.7 333.3 351 300C414.3 266.7 486.7 233.3 511.2 200C535.7 166.7 512.3 133.3 455.2 100C398 66.7 307 33.3 261.5 16.7L216 0L900 0L900 16.7C900 33.3 900 66.7 900 100C900 133.3 900 166.7 900 200C900 233.3 900 266.7 900 300C900 333.3 900 366.7 900 400C900 433.3 900 466.7 900 500C900 533.3 900 566.7 900 583.3L900 600Z"
            fill="#F7770F"
            stroke-linecap="round"
            stroke-linejoin="miter"
          ></path>
        </svg>
      </v-col>
    </v-row>
  </v-sheet>
</template>

<style scoped></style>
