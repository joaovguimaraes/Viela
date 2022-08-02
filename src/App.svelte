<script>
	import Home from "./components/home.svelte";
	import Atividades from "./components/atividades.svelte";
	import Institucional from "./components/institucional.svelte";
	import Footer from "./components/footer.svelte";
	import Historias from "./components/historias.svelte";
	import Equipe from "./components/equipe.svelte";
</script>

<main>
	<Home />
	<Institucional />
	<Atividades />
	<Historias />
	<Equipe />
	<Footer />
</main>

<style>
	:global(body) {
		margin: 0;
		padding: 0;
	}
</style>
