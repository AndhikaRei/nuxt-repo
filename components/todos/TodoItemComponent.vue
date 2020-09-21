<template>
	<tr>
		<td class="align-middle" v-bind:class="{'is-completed':todo.completed}">{{ todo.title }}</td>
		<td>
			<button class="btn btn-success" v-on:click="changeComplete" v-bind:class="{'btn-warning':!todo.completed, 'btn-danger':todo.completed}" >
				<i class="fa" v-bind:class="{'fa-check':!todo.completed, 'fa-window-close':todo.completed}" ></i>
			</button>
		</td>
		<td>
			<button @click="$emit('del-todo',todo.id)" class="btn btn-info">
				<i class="fa fa-trash"></i>
			</button>
		</td>
	</tr>
</template>

<script>
export default {
	data() {
		return {
			id : todo.id
		}
	},
	name: "TodoItem",
	props:["todo","id"], 
	methods: {
		changeComplete(){
			this.todo.completed = !this.todo.completed;
		}
	}
};
</script>

<style scoped>
.is-completed {
	text-decoration: line-through;
}
</style>
