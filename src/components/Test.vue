<template>
<div class="test">	
{{ msg }}
</div>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hola VueJs',
				usuario: {
					firstName: 'Fernando',
					lastName: 'De la Ostia'
				},
				myHtml: '<h3>hola vue</h3',
				showName: false,
				tasks: [
					{title: 'eat'},
					{title: 'dinner'},
					{title: 'shower'},
					{title: 'sleep'}
				]
				
			}
		},
// Funciones/metodos de VUE.JS, el cual usamos en el boton
		methods: {
			saludar(name) { 
				alert("Hello " + name)
				},
			typedEnter(e) {
				console.log('DIO UN ENTER');

			}
		},
		computed: {
			fullName() {
				return this.usuario.firstName + ' ' + this.usuario.lastName;
			}
		},
		props: {
			msg: {
				type: String,
				default: 'Mensaje por defecto'
			}
		}
	}
</script>

<style media="screen">
	.test{
		background-color: #eee;
	}
</style>