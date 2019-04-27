<template>
   <div>
       <h1>Witaj, {{ xyz }}</h1>
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
 
 props: ['xyz']
}
</script>