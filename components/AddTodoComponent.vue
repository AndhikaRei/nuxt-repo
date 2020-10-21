<template>
	<b-container class="mb-5">
		<b-row class="mt-4 justify-content-center">
			<b-col sm="12" md="10" lg="6"> 
				<b-card>
					<template #header>
						<h4 class="text-center font-weight-bold mb-0">Do You Have New Todo?</h4>
					</template>
					<b-card-body>
						<b-form  @submit="addTodo" class="mt-2">
							<b-form-group>
								<b-form-row class="justify-content-center">
									<b-form-input type="text" class="col-8" v-model="title" name="title" id="title"></b-form-input>
									<b-button variant="warning" class="col-3 ml-2" type="submit"> <i class="fa fa-plus"></i> Add</b-button>
								</b-form-row>
							</b-form-group>
						</b-form>
					</b-card-body>
				</b-card>
			</b-col>
		</b-row>
	</b-container>
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