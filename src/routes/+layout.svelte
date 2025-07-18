<script lang="ts">
	import '../app.css';
	import Cabecalhoteste from "./cabecalho/cabecalhoteste.svelte";
	import Rodapeteste from "./rodape/rodape.svelte";
	let { children } = $props();
</script>

<Cabecalhoteste/>
<Rodapeteste/>
<!-- Usado pra carregar componente antes de outros componentes -->
{@render children()}