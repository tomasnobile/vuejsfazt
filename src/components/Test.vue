<template>
<div>
	<div v-text="title"></div>
	<div v-if="showName">
		<p>{{usuario.firstName}}</p>
	</div>
	<div v-else>
	<p>No puedo mostrar el nombre, lo siento.</p>
</div>
<hr>
<ul>
	<li v-for="task in tasks">
		{{ task.title }}
	</li>
</ul>
</div>

</template>

<script>
	export default {
		data() {
			return {
				title: 'Hola VueJs',
				usuario: {
					firstName: 'Juan',
					lastName: 'Fernandez'
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
		}

	}
</script>

<style>
	

</style>