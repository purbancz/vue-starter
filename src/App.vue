<template>
	<div>
		<h1>Witaj w systemie do zapisów na zajęcia</h1>
		<p>Zaloguj się emailem <input type="email" v-model="email">
		<button @click="login()">Wchodzę</button></p>
		<h1>Witaj {{ email }}</h1>
		<a href="#"  @click="logout()">Wyloguj</a>
	</div>
</template>

<script>



export default {
	data() {
		  return {
		    email: '',
		    password: ''
		  };
	},
	methods: {
		  alertMyEmail() {
		    alert(this.email);
		  },
		  login() {
			  document.write("<h1>Witaj " + this.email + "</h1>");
			  }
	}
	
}


</script>

<style>
</style>
