<template>
	<div>
		<b-container class="mt-5">
			<h1></h1>
			<b-row>
				<b-col>
					<TodoList />
				</b-col>
			</b-row>
			<b-button @click="cancel()" class="float-right mt-3 mb-5" type="is-link">More Projects</b-button>
		</b-container>
	</div>
</template>
<script>

import TodoList from '@/pages/projects/vue-do/TodoList.vue'

export default {
  name: 'App',
  components: {
    TodoList
    
  },
  methods: {
	cancel(){
			this.$router.go(-1)
		}
  }
}
</script>

<style>
.container {
  margin-top: 1em;
}
</style>
