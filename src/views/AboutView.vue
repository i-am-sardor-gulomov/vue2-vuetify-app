<template>
  <div>
    <v-card max-width="500px" class="mx-auto mt-5" border-bottom="">
      <v-toolbar color="primary" dark flat>
        <v-toolbar-title> Card </v-toolbar-title>
      </v-toolbar>
      <v-divider></v-divider>
      <v-card-text>
        <v-text-field
          label="First name"
          :rules="rules"
          outlined
          dense
        ></v-text-field>
        <v-text-field label="Last name" outlined dense></v-text-field>
        <v-text-field label="Age" outlined dense type="number" min="1" max="100"></v-text-field>
        <v-radio-group inline label="Gender">
          <v-radio label="Male" value="1"></v-radio>
          <v-radio label="Female" value="2"></v-radio>
          <v-radio label="Other" value="3"></v-radio>
        </v-radio-group>
      </v-card-text>
      <v-divider></v-divider>
      <v-card-actions>
        <v-spacer></v-spacer>
        <v-btn color="primary">Submit</v-btn>
      </v-card-actions>
    </v-card>
  </div>
</template>
<script>
export default {
  data: () => ({
    rules: [
      (value) => !!value || "Required.",
      (value) => (value && value.length >= 3) || "Min 3 characters",
    ],
  }),
};
</script>