<template>
	<div class="container mt-4">
		<div class="row justify-content-center">
			<div class="col-12 col-sm-10 col-md-8 col-lg-5">
					<div class="card">
						<h2 class="card-header text-center font-weight-bold">
              This is All your To-do
            </h2>
						<div class="card-body text-center">
							<div class="table-responsive">
								<table class="table table-borderless">
									<thead>
										<tr>
											<th>Your Todo</th>
											<th>Completed</th>
											<th>Action</th>
										</tr>
									</thead>
									<tbody v-for="todo in todos" v-bind:key="todo.id">
										<TodoItem v-bind:todo="todo" v-bind:id="todo.id" v-on:del-todo="$emit('del-todo',todo.id)"/>
									</tbody>
								</table>
							</div>
						</div>
					</div>
			</div>
		</div>
	</div>
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