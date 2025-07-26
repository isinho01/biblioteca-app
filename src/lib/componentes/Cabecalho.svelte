<div class="principal">
	<img src="/Campus São Gonçalo do Amarante - Logo_Color Hor.png" alt="Logo do campus" />
	<h1>Sistema Bibliotecario | IFRN Campus São Gonçalo do Amarante</h1>
</div>
<div class ="bloco">
		<ul class="listas">
			<li>Buscar Livro</li>
		<li>Livros disponiveis para emprestimo</li>
		<li>Renovar emprestimo</li>
		</ul>
	<ul class="listas">
		<li>
			<a href="/destaques">Livros em Destaque</a>
		</li>
		<li>Recém Adquiridos</li>
		<li>Área do Usuário</li>
		<li>Contato</li>
	</ul>
</div>
<style>
	h1 {
		font-size: 25px;
		text-align: center;
	}
	.listas {
		margin-left: 20%;
		text-align: center;
		display: flex;
		list-style: none;
		gap: 40px;	
	}
	.listas  {
		margin:0;
		display:flex;
		justify-content: center;
		padding: 5px;
		background-color: #f0f0f0; 
	}
	.principal {
		padding: 3px;
		background-color: #228b22;
	}
	 @import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');
	.principal {
		background-color: #093800;
		display: flex;
		flex-wrap: wrap; /* quebra de linha em telas pequenas */
		align-items: center;
		padding: 1rem;
		min-height: 80px; /* Altura mínima ao invés de fixa */
	}

	.logo {
		max-width: 300px;
		width: 100%;
		height: auto; /* Mantém proporção */
		flex: 1; /* Ocupa espaço disponível */
		min-width: 150px;
	}

	.listas {
		display: flex;
		flex-wrap: wrap; /* quebra dos itens */
		justify-content: center;
		gap: 1rem;
		flex: 2;
	}

	.listas li {
		padding: 0.5rem 2rem;
		margin: 0.1rem; /* Espaçamento externo responsivo */
		background: rgba(255, 255, 255, 0.2);
		border-radius: 8px;
		text-align: center;
		transition: transform 0.3s ease;
		color: white;
		font-family: "Poppins", sans-serif;
	}

	.listas li:hover {
		transform: translateY(-3px);
		background: rgba(255, 255, 255, 0.3);
	}

	@media (max-width: 900px) {
		.listas {
			margin-top: 1rem !important;
			margin-left: 0 !important;
			width: 100%;
		}

		.listas li {
			padding: 0.5rem 1rem;
			margin: 0.25rem;
			font-size: 0.9rem;
		}
	}

	@media (max-width: 600px) {
		.logo {
			margin: 0 auto; /* Centraliza logo */
		}

		.listas {
			flex-direction: column; /* Itens em coluna */
			gap: 0.5rem;
		}

		.listas li {
			width: 90%;
			margin: 0.25rem auto;
		}
	}
</style>
