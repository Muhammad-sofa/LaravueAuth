<template>
     <form @submit.prevent="submitForm">
          <input v-model="form.name" placeholder="Name" />
          <span v-if="errors.name">{{ errors.name[0] }}</span>

          <input v-model="form.email" placeholder="Email" />
          <span v-if="errors.email">{{ errors.email[0] }}</span>

          <input type="password" v-model="form.password" placeholder="Password" />
          <span v-if="errors.password">{{ errors.password[0] }}</span>

          <button type="submit">Register</button>
     </form>
</template>

<script>
export default {
     data() {
          return {
               form: {
                    name: "",
                    email: "",
                    password: "",
               },
               errors: {},
          };
     },
     methods: {
          submitForm() {
               axios
                    .post("/register", this.form)
                    .then(() => {
                         // Success handling
                    })
                    .catch((error) => {
                         if (error.response.status === 422) {
                              this.errors = error.response.data.errors;
                         }
                    });
          },
     },
};
</script>
