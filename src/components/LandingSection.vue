<template>
  <v-sheet id="home" class="mb-n4">
    <v-row>
      <!-- Text content column -->
      <v-col cols="12" md="6" sm="12">
        <div style="min-height: 100px"></div>
        <v-container>
          <v-row class="mx-5 my-0 py-0 d-flex justify-center align-center text-center">
            <div class="text-h6 font-weight-light">
              HEMANT TRADERS | COMPLETE POST-PRESS SOLUTIONS | INDIA
            </div>
            <div class="text-h3 my-5">
              Connect with India's Trusted Film & Adhesives Supplier.
            </div>
            <div class="text-h6 font-weight-light paragraph">
              At Hemant Traders, we specialize in BOPP (Biaxially Oriented
              Polypropylene) and Polyester (PET) film conversions, catering to a
              wide range of industries. Our expertise includes lamination films,
              bookbinding and pasting adhesives, and UV coat solutions, designed
              to meet diverse application needs with precision and quality.
              Based in Pune, Maharashtra, India, we are committed to delivering
              top-notch products and exceptional service. Our solutions are
              tailored to enhance durability, aesthetics, and functionality,
              making us a trusted partner for packaging, publishing, and
              commercial printing industries. With a focus on quality,
              innovation, and customer satisfaction, Hemant Traders offers a
              comprehensive range of films, adhesives, and UV coats to support
              your business with reliable and efficient solutions.
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
                color="primary my-2"
                elevation="0"
                variant="outlined"
                href="https://wa.me/919422080922"
                target="_blank"
                rounded
                size="large"
              >
                <v-icon>mdi-whatsapp</v-icon>
                WhatsApp
              </v-btn>
            </v-col>
          </v-row>
        </v-container>
      </v-col>

      <!-- SVG content column -->
      <v-col md="6" class="hidden-sm-and-down">
        <svg
          id="visual"
          viewBox="0 0 900 800"
          width="900"
          height="800"
          xmlns="http://www.w3.org/2000/svg"
          xmlns:xlink="http://www.w3.org/1999/xlink"
          version="1.1"
        >
          <!-- Wave -->
          <path
            d="M849 1100L594.3 850C539.7 800 430.3 730 352 680C273.7 630 226.3 580 229.8 520C233.3 460 287.7 400 351 360C414.3 320 486.7 280 511.2 240C535.7 200 512.3 150 455.2 100C398 50 307 20 261.5 10L216 0L1200 0L1200 10C1200 20 1200 50 1200 100C1200 150 1200 200 1200 240C1200 280 1200 320 1200 360C1200 400 1200 460 1200 520C1200 580 1200 630 1200 680C1200 730 1200 800 1200 850L1200 900Z"
            fill="url(#wave-gradient)"
            stroke-linecap="round"
            stroke-linejoin="miter"
          ></path>
          <!-- Gradient for Wave -->
          <defs>
            <linearGradient id="wave-gradient" x1="0" y1="0" x2="0" y2="1">
              <stop offset="0%" stop-color="#F7770F" />
              <stop offset="100%" stop-color="#FF9A3E" />
            </linearGradient>
          </defs>

          <!-- Additional Decorative Elements -->
          <circle cx="200" cy="100" r="50" fill="#FFE4D3" opacity="0.5" />
          <circle cx="600" cy="450" r="40" fill="#FFD3BA" opacity="0.7" />
        </svg>
      </v-col>
    </v-row>
  </v-sheet>
</template>

<style scoped></style>
