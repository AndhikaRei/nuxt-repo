<template>
	<header>
		<b-navbar toggleable="sm" type="dark" class="justify-content-center bg-primary1">
			<a class="navbar-brand" href="#">Vue TodoList</a>
			<div id="nav" class="align-middle">
				<nuxt-link class="text-white" to="/about">About</nuxt-link>
				<nuxt-link class="text-white" to="/">Home</nuxt-link>
			</div>
		</b-navbar> 
	</header>   
</template>

<script>
export default {
	name: "HeaderComponent"
}
</script>

<style scoped>
.bg-primary1 {
	background-color : #42b883 ;
}
</style>