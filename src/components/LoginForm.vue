<template>
   <div>
       <label>Zaloguj się e-mailem</label>
       <input type="email" v-model="email">
       <button @click="enter()">{{ buttonLabelToDisplay }}</button>
   </div>
</template>

<script>
export default {
 data() {
     return {
         email: ''
     }
 },
  props: ['buttonLabel'],
 
 computed: {
	  buttonLabelToDisplay() {
	    return this.buttonLabel || 'Zaloguj się';  
	  }
	},
	
 methods: {
     enter() {
         this.$emit('login', this.email);
     },
     
 },

}
</script>