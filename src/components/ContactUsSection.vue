<template>
  <v-sheet id="contactus" class="text-center py-16" color="primary">
    <div class="text-white text-h4 font-weight-medium">
      Contact Us
    </div>

    <div class="text-center text-body-1 mb-10">
      Have any queries? Get in touch today.
    </div>

    <v-container>
      <v-row>
        <v-col cols="6">
          <v-text-field
            v-model="form.name"
            label="Your Name*"
            dark
            hide-details
            outlined
          />
        </v-col>

        <v-col cols="6">
          <v-text-field
            v-model="form.email"
            label="Email Address*"
            dark
            hide-details
            outlined
          />
        </v-col>

        <v-col cols="6">
          <v-text-field
            v-model="form.phone"
            label="Phone Number*"
            dark
            hide-details
            outlined
          />
        </v-col>

        <v-col cols="6">
          <v-text-field
            v-model="form.option"
            label="Option*"
            dark
            hide-details
            outlined
          />
        </v-col>

        <v-col cols="12">
          <v-textarea
            v-model="form.message"
            label="Your Message..."
            rows="4"
            dark
            hide-details
            outlined
          />
        </v-col>
      </v-row>
    </v-container>
    <v-btn
  class="px-10 text-body-1 mt-5"
  color="accent"
  height="55"
  :loading="isLoading"
  :disabled="isLoading"
  @click="submitForm"
>
  GET IN TOUCH
</v-btn>

  </v-sheet>
</template>

<script setup>
import { ref } from "vue";

const form = ref({
  name: "",
  email: "",
  phone: "",
  option: "",
  message: "",
});
const validateForm = () => {
  if (!form.value.name || !form.value.email || !form.value.phone) {
    alert("Please fill out all required fields.");
    return false;
  }
  return true;
};
const isLoading = ref(false);

const submitForm = async () => {
  if (!validateForm()) return;

  const webAppUrl = "https://script.google.com/macros/s/AKfycbyF3aTKVzs94wncqNKKGAAw3044GPbeeXssBtv6diwmXDC60K4OOTAG5QQvaT6rBH5zYA/exec";
  try {
    const response = await fetch(webAppUrl, {
      method: "POST",
      body: JSON.stringify(form.value),
      headers: { "Content-Type": "application/json" },
    });

    const result = await response.json();
    if (result.status === "success") {
      alert("Form submitted successfully!");
      form.value = { name: "", email: "", phone: "", option: "", message: "" }; // Reset the form
    } else {
      alert(`Error: ${result.message}`);
    }
  } catch (error) {
    alert("Failed to submit the form. Please try again later.");
  }
};

</script>
