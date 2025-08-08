<script lang="ts">
	import { onMount } from "svelte";

    let livros:{titulo:string, autor:string, descricao:string, createdAt:string}[]=$state([]) // Inicializa a variável livros como um array vazio
    async function load() { // Função para carregar dados, usado para criar uma funcao assincrona
       try{
         const resposta=await fetch("https://6895f7a1039a1a2b2890fcbe.mockapi.io/api/v1/livro")
         const livros = await resposta.json();
         return livros; // Retorna os dados dos livros
    }catch(e){
        console.error("Erro ao buscar dados:", e);
    }
    }
    onMount(async () => {
        livros = await load(); // Chama a função load para obter os dados dos livros
    });   
</script>

{#each livros as livro}
   <div>
    <h1 class="text-xl font-bold text-blue-700 mb-2">{livro.titulo}</h1>
    <p class="text-gray-700 mb-1">{livro.autor}</p>
    <p class="text-gray-600 mb-1">{livro.descricao}</p>
    <p class="text-xs text-gray-400">{livro.createdAt}</p>
</div>
{/each}

