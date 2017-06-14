<template>
<div class="col-md-12">
  <div class="from-inline">
    <h3>Sign In</h3>
    <div class="form-group">
      <input type="text" placeholder="email" class="form-control" v-model="email" />
    </div>
    <div class="form-group">
      <input type="password" placeholder="password" class="form-control" v-model="password">
    </div>
    <button class="btn btn-primary btn-block " @click="signIn">Sign In</button>
  </div>
  <br>
  <router-link to="/signup">Not a user? Sign up</router-link>
  <br>
  <p>{{error.message}}</p>
</div>
</template>

<script>
import {
  firebaseApp
} from '../firebaseApp'

export default {
  data() {
    return {
      email: '',
      password: '',
      error: {
        message: ''
      }
    }
  },
  methods: {
    signIn() {
      firebaseApp.auth().signInWithEmailAndPassword(this.email, this.password)
        .catch(error => {
          this.error = error
        })
    }
  }
}
</script>
