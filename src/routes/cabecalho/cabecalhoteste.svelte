<div class="principal">
	<img
		class="logo"
		src="/Campus São Gonçalo do Amarante - Logo_Negat Hor.png"
		alt="Logo do campus"
	/>
	<ul class="listas">
		<li>Recém Adquiridos</li>
		<li>Área do Usuário</li>
		<li>Contato</li>
	</ul>
</div>

<style>
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
