<template>
  <v-sheet id="about" class="py-16" color="secondary">
    <!-- Hero Section -->
    <v-container>
      <div class="text-h5 font-weight-bold text-primary mb-4">
        HEMANT TRADERS COMPLETE POST PRESS SOLUTIONS | INDIA
      </div>
      <div class="text-h3 font-weight-bold text-primary mb-6">
        Leading Supplier of Films, Adhesives, and UV Coats
      </div>
      <div class="text-body-1 font-weight-regular text-dark mb-8">
        Our dedicated team provides innovative, eco-friendly solutions with
        unparalleled customer support. Let us help you take your business to the
        next level with our premium products and services.
      </div>
      <v-btn
        class="mt-4"
        color="primary"
        rounded
        size="x-large"
        href="#services"
        elevation="2"
        aria-label="Learn More About Us"
      >
        Learn More About Us
      </v-btn>
    </v-container>

    <!-- What We Do Section -->
    <v-container id="services" class="mt-12">
      <div class="text-h4 font-weight-bold text-center mb-8 text-primary">
        Why Choose Hemant Traders?
      </div>
      <v-row>
        <v-col
          v-for="item in whatWeDo"
          :key="item.title"
          class="d-flex justify-center align-center"
          cols="12"
          md="4"
        >
          <v-card
            class="ma-4 pa-6 text-center elevation-10"
            :color="'white'"
            dark
            rounded
            max-width="400"
            tile
          >
            <v-card-title class="justify-center">
              <v-icon large class="mb-3" :color="item.iconColor">{{
                item.icon
              }}</v-icon>
            </v-card-title>
            <v-card-text>
              <div class="text-h6 font-weight-bold text-primary">
                {{ item.title }}
              </div>
              <div class="text-body-1 text-medium-emphasis">
                {{ item.description }}
              </div>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-container>

    <!-- CTA Section -->
    <v-container class="mt-12" fluid>
      <v-row>
        <v-col class="d-flex justify-center">
          <v-btn
            color="accent"
            rounded
            size="x-large"
            @click="dialog = true"
            elevation="2"
            aria-label="Get in Touch with Us"
          >
            Get in Touch with Us
          </v-btn>
        </v-col>
      </v-row>
    </v-container>

    <!-- Dialog with Contact Options -->
    <v-dialog v-model="dialog" max-width="400px" persistent>
      <v-card>
        <v-card-title class="text-h6 text-center">Contact Us</v-card-title>
        <v-card-text>
          <v-list lines="three">
            <v-list-item>
              <v-list-item-title>
                <a
                  href="mailto:info@hemanttraders.com"
                  class="text-decoration-none text-primary"
                  aria-label="Email"
                >
                  <v-icon left>mdi-email</v-icon> Mail
                </a>
              </v-list-item-title>
            </v-list-item>
            <v-list-item>
              <v-list-item-title>
                <a
                  href="tel:+911234567890"
                  class="text-decoration-none text-primary"
                  aria-label="Call"
                >
                  <v-icon left>mdi-phone</v-icon> Call
                </a>
              </v-list-item-title>
            </v-list-item>
            <v-list-item>
              <v-list-item-title>
                <a
                  href="https://wa.me/911234567890"
                  target="_blank"
                  class="text-decoration-none text-primary"
                  aria-label="WhatsApp"
                >
                  <v-icon left>mdi-whatsapp</v-icon> WhatsApp
                </a>
              </v-list-item-title>
            </v-list-item>
          </v-list>
        </v-card-text>
        <v-card-actions>
          <v-btn color="primary" text @click="dialog = false" aria-label="Close"
            >Close</v-btn
          >
        </v-card-actions>
      </v-card>
    </v-dialog>
  </v-sheet>
</template>

<script setup>
import { ref } from "vue";

const dialog = ref(false);

const whatWeDo = [
  {
    title: "Eco-Friendly & Future-Focused",
    description:
      "At Hemant Traders, we prioritize sustainability by not selling Single-Use Plastics (SUPs). Instead, we offer biodegradable, eco-friendly lamination and window films. Our UV Coats provide a sustainable alternative to plastic, offering superior protection and durability. We are committed to delivering high-quality, environmentally conscious products that support your business’s green goals.",
    icon: "mdi-leaf",
    iconColor: "#00FFFF", // third color
  },
  {
    title: "Problem Solvers",
    description:
      "With over 40 years of expertise in the film conversion industry, we are committed to providing innovative solutions that meet your unique business needs. Our team works hand-in-hand with you to deliver custom products, including adhesives for both manual and machine applications, ensuring that your processes run smoothly and efficiently. Trust Hemant Traders for top-quality adhesives for lamination, book binding, and pasting, designed to boost performance and add value to your business operations.",
    icon: "mdi-lightbulb-on",
    iconColor: "#E52F37", // accent color
  },
  {
    title: "Unmatched Service",
    description:
      "We pride ourselves on fast lead times, great value, and expert advice. Our established distribution channels and strong partnerships with leading Indian companies ensure long-term, secure relationships. This solid foundation enables us to deliver high-quality, cost-effective services to our customers worldwide. We’re committed to providing exceptional customer service and supporting your business in a rapidly evolving global market.",
    icon: "mdi-account-check",
    iconColor: "#FE9900", // primary color
  },
];
</script>

<style scoped>
/* Hero Section - Background, Padding, and Centering */
#about {
  background-size: cover;
  background-position: center;
  text-align: center;
}

.text-primary {
  color: #fe9900 !important; /* primary color */
}

.text-accent {
  color: #e52f37 !important; /* accent color */
}

.text-third {
  color: #00ffff !important; /* third color */
}

.text-white {
  color: white !important;
}

/* Hover effects for cards */
.v-card {
  transition: transform 0.3s ease-in-out;
}

.v-card:hover {
  transform: scale(1.05);
}

/* Adjust button styles */
.v-btn {
  font-size: 16px;
  letter-spacing: 0.5px;
}

.text-dark {
  color: #333 !important;
}

.text-body-1.text-medium-emphasis {
  color: rgba(0, 0, 0, 0.6);
}
</style>
