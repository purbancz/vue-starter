<template>
   <div>
       <h1>Witaj, {{ username }}</h1>
		<a @click="getOut()">Wyloguj</a>
   </div>
</template>

<script>
export default {


	
 methods: {
	 getOut() {
         this.$emit('logout');
     },
     
 },
 
 props: ['username']
}
</script>