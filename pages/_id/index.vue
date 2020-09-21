<template>
		<div>
			<div class="container mt-4">
				<div class="row justify-content-center">
					<div class="col-12 col-sm-10 col-md-8 col-lg-5">
						<div class="card">
							<h2 class="card-header text-center font-weight-bold">
              {{ todo.title }}
            	</h2>
							<div class="card-body">
								<div class="table-responsive">
									<table class="table table-borderless">
										<tr v-bind:class="{'bg-danger':!todo.completed, 'bg-success':todo.completed}" >
											<th>Completed</th>
											<td>{{todo.completed}}</td>
										</tr>
										<tr>
											<th>Id</th>
											<td>{{todo.id}}</td>
										</tr>
									</table>
								</div>
								<button class="btn btn-primary">
									<i class="fa fa-arrow-left"><nuxt-link class="text-white" to="/"> Back to TodoList</nuxt-link></i>
								</button>
							</div>
						</div>
					</div>
				</div>
			</div>
			
		</div>
</template>
<script>
import axios from 'axios';

export default {
	data(){
		return {
			todo : {}
		}
	},
	created() {
		axios.get(`https://jsonplaceholder.typicode.com/todos/${this.$route.params.id}`)
			.then(res => this.todo = res.data)
			.catch(err => console.log(err));
	}
}
</script>

<style scoped>
.card-header {
	background-color : #42b883 ;
}
</style>