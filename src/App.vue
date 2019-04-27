<template>
	<div v-if="log == false">
		<h1>Witaj w systemie do zapisów na zajęcia</h1>
		<p>Zaloguj się emailem <input type="email" v-model="email">
		<button @click="login()">Wchodzę</button></p>
		
		
	</div>
	<div v-else>
		<h1>Witaj {{ email }}</h1>
		<a href=""  @click="logout()">Wyloguj</a>
	</div>
</template>

<script>

import "milligram";


export default {
	data() {
		  return {
		    email: '',
		    password: '',
		    log: false
		  };
	},
	methods: {
		alertMyEmail() {
			alert(this.email);
		},
		login() {
			this.log = true;
		},
		logout() {
			this.log = false;
		},
	}
	
}


</script>

<style>
</style>
