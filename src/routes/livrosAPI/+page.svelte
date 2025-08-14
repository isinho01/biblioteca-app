<script lang="ts">
	import { onMount } from 'svelte';

	// Lista de livros disponíveis, carregados da API
	let livros: {
		id?: number;
		titulo: string;
		autor: string;
		descricao: string;
		createdAt: string;
	}[] = [];

	// Lista de livros reservados pelo usuário (apenas em memória/local)
	let livrosReservados: {
		id?: number;
		titulo: string;
		autor: string;
		descricao: string;
		createdAt: string;
	}[] = [];

	// Função para carregar os livros da API
	async function load() {
		try {
			const resposta = await fetch('https://6895f7a1039a1a2b2890fcbe.mockapi.io/api/v1/livro');
			const livros = await resposta.json();
			return livros;
		} catch (e) {
			console.error('Erro ao buscar dados:', e);
		}
	}

	// Função para reservar um livro
	// Adiciona o livro à lista de reservados se ainda não estiver nela
	function reservarLivro(livro) {
		if (!livrosReservados.find((l) => l.id === livro.id)) {
			livrosReservados = [...livrosReservados, livro];
			alert('Livro reservado com sucesso!');
		} else {
			alert('Este livro já está reservado.');
		}
	}

	// Carrega os livros ao montar o componente
	onMount(async () => {
		livros = await load();
	});
</script>

<!-- Lista de livros disponíveis -->
<h2 class="mt-4 mb-2 text-lg font-bold">Livros disponíveis</h2>
{#each livros as livro}
	<div class="mb-4 rounded border p-2">
		<h1 class="mb-2 text-xl font-bold text-blue-700">{livro.titulo}</h1>
		<p class="mb-1 text-gray-700">{livro.autor}</p>
		<p class="mb-1 text-gray-600">{livro.descricao}</p>
		<p class="text-xs text-gray-400">{livro.createdAt}</p>
		<!-- Botão para reservar o livro -->
		<button
			class="mt-2 rounded bg-green-500 px-3 py-1 text-white"
			on:click={() => reservarLivro(livro)}
		>
			Reservar
		</button>
	</div>
{/each}

<!-- Lista de livros reservados -->
{#if livrosReservados.length > 0}
	<h2 class="mt-8 mb-2 text-lg font-bold">Livros reservados</h2>
	{#each livrosReservados as livro}
		<div class="mb-2 rounded border border-green-500 bg-green-50 p-2">
			<h1 class="mb-1 text-base font-bold text-green-700">{livro.titulo}</h1>
			<p class="mb-1 text-gray-700">{livro.autor}</p>
		</div>
	{/each}
{/if}
