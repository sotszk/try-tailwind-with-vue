<template>
  <div class="container">
    <h1 class="title">Register</h1>

    <form class="form mt-4">
      <div class="flex">
        <label>
          <div class="text-sm mb-1">FirstName</div>
          <input class="form-input" type="text" v-model="form.firstName" placeholder="Taro"/>
        </label>
        <label class="ml-4">
          <div class="text-sm mb-1">LastName</div>
          <input class="form-input" type="text" v-model="form.lastName" placeholder="Suzuki"/>
        </label>
      </div>

      <label class="block mt-4">
        <div class="text-sm mb-1">Email</div>
        <input class="form-input form-input--full" type="email" v-model="form.email" placeholder="hogehoge@gmail.com"/>
      </label>

      <label class="block mt-4">
        <div class="text-sm mb-1">PhoneNumber</div>
        <input class="form-input" type="text" v-model="form.phoneNumber" placeholder="000-0000-0000"/>
      </label>

      <label class="block mt-4">
        <div class="text-sm mb-1">Password</div>
        <input class="form-input" type="password" v-model="form.password" placeholder=""/>
      </label>

      <footer class="mt-4">
        <input @click.prevent="() => submit()" class="submit-btn" type="submit" value="Send">
      </footer>
    </form>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      form: {
        firstName: '',
        lastName: '',
        email: '',
        phoneNumber: '',
        password: '',
      }
    }
  },
  methods: {
    submit() {
      console.log(this.form);
    }
  }
};
</script>

<style src="./style.css"></style>

<style scoped>
.container {
  @apply p-6;
}
.title {
  @apply font-bold text-3xl;
}
.form {
  @apply border border-gray-400 rounded p-4;
}
.form-input {
  @apply appearance-none border border-gray-400 rounded py-1 px-2;
}
.form-input:focus {
  @apply outline-none shadow-outline;
}
.form-input--full {
  @apply w-full;
}
.submit-btn {
  @apply transition duration-200 ease-in-out rounded bg-teal-600 text-white font-bold py-2 px-4 cursor-pointer;
}
.submit-btn:hover {
  @apply bg-teal-700;
}

</style>
