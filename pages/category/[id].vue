<script lang="ts" setup>
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
  <div>
    {{ employee.firstName }}
  </div>
</template>

<style scoped></style>
