<template>
	<div v-if="isAuthenticated == false">
	<h1>Witaj w systemie do zapisów na zajęcia</h1>
		<login-form @login="logMeIn($event)" :button-label="'Wejdź'"></login-form>
		<login-form @login="logMeIn($event)" :button-label="'Wleć'"></login-form>
		<login-form @login="logMeIn($event)" :button-label="'Zaloguj się jak człowiek'"></login-form>
		<login-form @login="logMeIn($event)" ></login-form>
	</div>
	<div v-else>
		<!-- <h1>Witaj, {{ email }}</h1> -->
		<!-- <a @click="logMeOut()">Wyloguj</a> -->
		
		<logged-in @logout="logMeOut()" :xyz="email"></logged-in>
		
	</div>
</template>

<script>

import LoginForm from "./components/LoginForm";
import LoggedIn from "./components/LoggedIn";

import "milligram";



export default {
	components: {LoginForm, LoggedIn},
	data() {
		  return {
		    email: '',
		    password: '',
		    isAuthenticated: false
		  };
	},
	methods: {
		logMeOut() {
			this.isAuthenticated = false;
			this.email = '';
		},
		
		logMeIn(username) {
			this.isAuthenticated = true;
			this.email = username;
			}
	}
	
}


</script>

<style>
</style>
