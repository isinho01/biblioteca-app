<script lang="ts">
	import '../app.css';
	import Cabecalho from "../lib/componentes/Cabecalho.svelte";
	import Rodape from "../lib/componentes/Rodape.svelte";
	let { children } = $props();
</script>

<Cabecalho/>

<!-- Usado pra carregar componente antes de outros componentes -->
{@render children()}
<Rodape/>