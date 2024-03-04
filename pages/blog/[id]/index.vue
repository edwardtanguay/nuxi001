<script setup>
const employees = [
	{
		id: 1,
		firstName: "Frank",
	},
	{
		id: 2,
		firstName: "Anne",
	},
	{
		id: 3,
		firstName: "Roger",
	},
];

const route = useRoute();

const employee = employees.find((m) => m.id === Number(route.params.id));
</script>

<template>
	<h1>Blog Entry</h1>
	<nav>
		<ul class="flex gap-1">
			<li v-for="emp in employees" :key="emp.id">
				<NuxtLink :to="`${emp.id}`" class="underline"
					>{{ emp.firstName }}</NuxtLink
				>
			</li>
		</ul>
	</nav>
	<p>showing id#{{ $route.params.id }}</p>
	<p>First Name: {{ employee.firstName }}</p>
</template>

<style scoped></style>
