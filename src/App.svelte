<script>
	import { Route, Router } from 'svelte-routing'

	import Create from './create/Create.svelte'
	import Detail from './detail/Detail.svelte'
	import Library from './library/Library.svelte'

	export let url = ''
</script>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>

<Router {url}>
	<main>
		<Route path="/create">
			<Create />
		</Route>
		<Route path="/books/:id" let:params>
			<Detail id={params.id} />
		</Route>
		<Route path="/">
			<Library />
		</Route>
	</main>
</Router>