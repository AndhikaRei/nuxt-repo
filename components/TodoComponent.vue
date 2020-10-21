<template>
	<b-container class="mt-4">
		<b-row class="justify-content-center">
			<b-col sm="12" md="10" lg="5">
				<b-card>
					<template #header>
						<h4 class="text-center font-weight-bold mb-0">This is All your To-do</h4>
					</template>
					<b-card-body class="text-center py-0 px-0">
						<div class="table-responsive-sm ">
							<table class="table table-borderless table-sm">
								<thead>
									<b-tr>
										<b-th colspan="3">Your Todo</b-th>
										<b-th>Stat</b-th>
										<b-th>Opt</b-th>
									</b-tr>
								</thead>
								<tbody v-for="todo in todos" :key="todo.id">
									<TodoItem :todo="todo" :id="todo.id" @del-todo="$emit('del-todo',todo.id)"/>
								</tbody>
							</table>
						</div>
					</b-card-body>
				</b-card>
			</b-col>
		</b-row>
	</b-container>
</template>

<script>
import TodoItem from './todos/TodoItemComponent.vue'
export default {
	name : "Todo",
	components : {
		TodoItem,
	},
	props:["todos"]
}
</script>

<style scoped>
.card-header {
	background-color : #42b883 ;
}
</style>