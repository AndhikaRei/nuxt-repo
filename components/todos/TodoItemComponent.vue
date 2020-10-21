<template>
	<b-tr>
		<b-td colspan="3" class="align-middle" :class="{'is-completed':todo.completed}">{{ todo.title }}</b-td>
		<b-td>
			<b-button @click="changeComplete" :class="{'btn-success':!todo.completed, 'btn-danger':todo.completed}" >
				<i class="fa" :class="{'fa-check':!todo.completed, 'fa-window-close':todo.completed}" ></i>
			</b-button>
		</b-td>
		<b-td>
			<b-button variant="info" @click="$emit('del-todo',todo.id)">
				<i class="fa fa-trash"></i>
			</b-button>
		</b-td>
	</b-tr>
</template>

<script>
export default {
	data() {
		return {
		}
	},
	name: "TodoItem",
	props:["todo"], 
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
