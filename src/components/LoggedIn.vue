<template>
   <div>
   		<p>test</p>
       <!-- <h1>Witaj, {{ authenticatedUsername }}</h1> -->
		<a @click="getOut()">Wyloguj-comp</a>
   </div>
</template>

<script>
export default {

	
 methods: {
	 getOut() {
         this.$emit('logout');
     },
     
 },
 
 //props: ['authenticatedUsername']
}
</script>