<template>
    <div class="d-flex justify-center">
      <v-card width="500" height="400">
        <v-card-title> Sign In </v-card-title>
          <v-card-text>
            <v-text-field label="Email or phone number" outlined></v-text-field>
          <v-text-field v-model="form.password" label="Password" :append-icon="show1 ? 'mdi-eye' : 'mdi-eye-off'"
              :type="show1 ? 'text' : 'password'" @click:append="show1 = !show1" outlined>
          </v-text-field>
          <v-card-actions>
        <v-btn @click="gotoDashbord" width="450" class="mr-2" color="success" >Sign In</v-btn>
      </v-card-actions>
        </v-card-text>
      </v-card>
    </div>
  </template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      show1: false,
      show2: false,
      form: {
        email: '',
        password: '',
      },
    }
  },
  methods: {
    gotoDashbord() {
      this.$router.push('/dashbord')
    }
  },
}
</script>