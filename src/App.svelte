<script>
	import Home from "./components/home.svelte";
	import Atividades from "./components/atividades.svelte";

	import Institucional from "./components/institucional.svelte";
	import Footer from "./components/footer.svelte";
</script>

<main>
	<Home />

	<Atividades/>
	<Institucional />
	<Footer />

</main>

<style>
	:global(body) {margin: 0; padding: 0; }
</style>
