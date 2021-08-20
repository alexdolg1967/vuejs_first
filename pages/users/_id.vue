<template>
	<div>
		<h1>Пользователь  {{ id }}</h1>
	</div>
</template>

<script>
export default {
	validate({ params }) {
    // Must be a number
    return /^\d+$/.test(params.id)
  },
	computed: {
		id() {
			return this.$route.params.id
		}
	},
}
</script>