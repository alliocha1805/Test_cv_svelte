<script>
	import Header from './Header.svelte';
	import './styles.css';
</script>

<div class="app" lang="fr">
	<Header />

	<main>
		<slot />
	</main>

	<footer>
	</footer>
</div>

<style>
</style>
