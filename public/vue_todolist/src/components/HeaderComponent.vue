<template>
	<header>
		<nav class="justify-content-center navbar navbar-expand-sm navbar-dark bg-primary1">
			<a class="navbar-brand" href="#">Vue TodoList</a>
			<div id="nav">
				<router-link to="/">Home</router-link> |
				<router-link to="/about">About</router-link>
			</div>
		</nav>  
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