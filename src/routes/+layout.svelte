<script lang="ts">
	import '../app.css';
	import Cabecalhoteste from "./cabecalho/cabecalhoteste.svelte";
	let { children } = $props();
</script>

<Cabecalhoteste/>
<!-- Usado pra carregar componente antes de outros componentes -->
{@render children()}