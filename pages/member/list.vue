<template>
	<h1>Member List</h1>

  <v-data-table :headers="headers" :items="items">
		<template v-slot:item.actions="{ item }">
      <v-icon size="small" class="me-2" @click="">
        mdi-pencil
      </v-icon>
      <v-icon size="small" @click=""> mdi-delete </v-icon>
    </template>
	</v-data-table>
</template>

<script setup>
	const headers = [
		{ title: 'ID', value: 'id' },
		{ title: 'Name', value: 'name' },
		{ title: 'Nickname', value: 'nickname' },
		{ title: 'Actions', value: 'actions' }
	]
	
	// TODO - get data from API	
	const items = [
		{ id: 1, name: "John Doe", nickname: 'Johnny'},
		{ id: 1, name: "Test Name", nickname: 'Testy'}
	]
	
</script>