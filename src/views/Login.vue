//login.vue
<template>
  <div class="row justify-content-md-center">
    <div class="col-md-12">
      <div class="card">
        <div class="card-body">
          <h1><b>Masuk Sekarang</b></h1>
          <p>Masuk dan nikmati fitur kami</p>
          <div v-if="loginFailed" class="alert alert-danger">
            Email atau Password Anda salah.
          </div>
          <form @submit.prevent="login">
            <div class="row">
              <div class="col-md-6">
                <div class="form-group">
                  <label for="name">Email</label>
                  <input
                    type="email"
                    class="form-control"
                    placeholder="Contoh : Contoh: bambang@gmail.com"
                    v-model="user.email"
                  />
                  <div v-if="validation.email" class="mt-2 alert alert-danger">
                    Masukkan Email
                  </div>
                </div>
                <button type="submit" class="btn btn-success">
                  Masuk Sekarang
                </button>
              </div>
              <div class="col-md-6">
                <div class="form-group">
                  <label for="password">Password</label>
                  <input
                    type="password"
                    class="form-control"
                    v-model="user.password"
                    placeholder="Masukkan Password"
                  />
                  <div
                    v-if="validation.password"
                    class="mt-2 alert alert-danger"
                  >
                    Masukkan Password
                  </div>
                </div>
              </div>
            </div>
          </form>
        </div>
      </div>
    </div>
    <div class="col-md-12" style="padding-top: 50px; padding-botton: 150px">
      <div>
        <b><h2>Cerita Kerabat AGROS</h2></b>
        <div class="row">
          <div class="col-sm-6">
            <img alt="Vue logo" src="../assets/4.png" />
          </div>
          <div class="col-sm-6">
            <p class="card-text" style="margin: auto; padding: 100px 0">
              Terinspirasi dari arah mata angin yang membawa pada satu
              destinasi, Agros akan terus bergerak menciptakan pemerataan
              ekonomi sehingga bisa menjadi penghubung para stakeholders dalam
              aktivitas muatan berat, mulai dari shipper, transporter, driver,
              mitra pemeliharan, seller dan buyer intermoda yang menjangkau
              seluruh penjuru Nusantara.
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  name: 'Login',

  data() {
    return {
      //state loggedIn with localStorage
      loggedIn: localStorage.getItem('loggedIn'),
      //state token
      token: localStorage.getItem('token'),
      //state user
      user: [],
      //state validation
      validation: [],
      //state login failed
      loginFailed: null,
    };
  },
  methods: {
    login() {
      if (this.user.email && this.user.password) {
        axios
          .get('http://localhost:8001/sanctum/csrf-cookie')
          .then((response) => {
            //debug cookie
            console.log(response);

            axios
              .post('http://localhost:8001/api/login', {
                email: this.user.email,
                password: this.user.password,
              })
              .then((res) => {
                //debug user login
                console.log(res);

                if (res.data.success) {
                  //set localStorage
                  localStorage.setItem('loggedIn', 'true');

                  //set localStorage Token
                  localStorage.setItem('token', res.data.token);

                  //change state
                  this.loggedIn = true;

                  //redirect dashboard
                  return this.$router.push({ name: 'dashboard' });
                } else {
                  //set state login failed
                  this.loginFailed = true;
                }
              })
              .catch((error) => {
                console.log(error);
              });
          });
      }

      this.validation = [];

      if (!this.user.email) {
        this.validation.email = true;
      }

      if (!this.user.password) {
        this.validation.password = true;
      }
    },
  },

  //check user already logged in
  mounted() {
    if (this.loggedIn) {
      return this.$router.push({ name: 'App' });
    }
  },
};
</script>
