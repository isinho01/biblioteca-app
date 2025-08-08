<script lang="ts">
	import { onMount } from "svelte";

    let usuario:{nome:string, cpf:number, senha:string, email:string, matricula: number, telefone: number}[]=$state([]) // Inicializa a variável livros como um array vazio
    async function load() { // Função para carregar dados, usado para criar uma funcao assincrona
       try{
         const resposta=await fetch("https://6895f7a1039a1a2b2890fcbe.mockapi.io/api/v1/usuario")
         const usuario = await resposta.json();
         return usuario; // Retorna os dados dos livros
    }catch(e){
        console.error("Erro ao buscar dados:", e);
    }
    }
    onMount(async () => {
        usuario = await load(); // Chama a função load para obter os dados dos livros
    });   
</script>

{#each usuario as usuario}
   <div>
    <h1 class="text-xl font-bold text-blue-700 mb-2">{usuario.nome}</h1>
    <p class="text-gray-700 mb-1">{usuario.cpf}</p>
    <p class="text-gray-600 mb-1">{usuario.senha}</p>
    <p class="text-xs text-gray-400">{usuario.email}</p>
    <p class="text-xs text-gray-400">{usuario.matricula}</p>
    <p class="text-xs text-gray-400">{usuario.telefone}</p>
</div>
{/each}

