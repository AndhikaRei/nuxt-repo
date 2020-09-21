<template>
	<div class="container mb-5">
		<div class="row mt-4 justify-content-center">
			<div class="col-12 col-sm-10 col-md-8 col-lg-6">
				<div class="card">
					<h3 class="card-header text-center font-weight-bold">Do You Have New Todo?</h3>
					<div class="card-body">
						<form  @submit="addTodo" class="mt-4">
							<div class="form-group">
								<div class="form-row justify-content-center">
									<input type="text" class="col-8 form-control" v-model="title" name="title" id="title">
									<button class="btn btn-warning col-3 ml-2" type="submit"> <i class="fa fa-plus"></i> Add Todo</button>
								</div>
							</div>
						</form>
					</div>
				</div>
			</div>  
		</div>
	</div>
</template>

<script>
// import { v4 as uuidv4 } from 'uuid';
export default {
	name: "AddTodo",
	data(){
		return {
			title:''
		}
	},
	methods : {
		addTodo(e){
			console.log(5);
			e.preventDefault();
			const newTodo = {
				// id : uuidv4(),
				title : this.title,
				completed : false
			}
			this.$emit('add-todo',newTodo);
			this.title = '';
		}
	}
}
</script>

<style scoped>
.card-header {
	background-color : #42b883 ;
}
</style>