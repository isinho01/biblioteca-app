<script lang="ts">
	
	export let titulo: string;
	export let subtitulo: string;
</script>

<div class="primeiradiv">
  <div class="cabecalho-flex">
	<div class="titulosIniciais">
	  <h1>{titulo}</h1>
	  <h2>{subtitulo}</h2>
	  <h3 class="descricao">A Biblioteca IFRN-SGA é uma biblioteca online criada com o propósitos de democratizar o acesso à leitura, ao conhecimento e à informação. Nossa missão é conectar leitores de todas as idades a um vasto acervo digital, reunindo obras clássicas, contemporâneas, acadêmicas e independentes em um único lugar, acessível a qualquer hora e de qualquer lugar.</h3>
	</div>
	<img id="mulher" src="/retrato-jovem-mulher-lendo-um-livro.png" alt="mulher com livro">
  </div>
</div>

<div class="livros_populares_principal">
	<h3 class="tituloPopulares">Títulos Populares</h3>
	<div class="livros_populares">
		<img src="/domcasmurrolivro.jpg" alt="Dom Casmurro" />
		<img src="/pequenacoreografialivro.jpg" alt="Pequena Coreografia" />
		<img src="/arianalivro.jpg" alt="Ariana" />
		<img src="/linuxlivro.jpg" alt="Linux" />
		<img src="/anittalivro.jpeg" alt="Anitta" />
		<img src="/aguavivalivro.jpg" alt="Água Viva" />
	</div>
</div>


<div class="experimente-container">
	<div class="experimente-box">
		<h2>Experimente Nosso Sistema!</h2>
		<button class="experimente-btn">CADASTRE-SE E<br>FAÇA PARTE</button>
	</div>
</div>

<style>
	@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');
	
	:global(html) {
		font-family: 'Poppins', sans-serif;
		margin: 0;
		padding: 0;
	}
	
	.primeiradiv {
		background-color: #059a43;
	}

	.primeiradiv h1 {
		font-weight: 1000;
		color: white;
		font-size: 100px;
		margin-left: 10%;
	}
	 
	.primeiradiv h2 {
		color: white;
		margin-left: 10%;
	}

	.primeiradiv h3 {
		color: white;
		font-family: 'Poppins', sans-serif;
		font-weight: 400;
		margin-left: 40px;
		font-size: large;
		display: flex;
	}

   .cabecalho-flex {
	   display: flex;
	   flex-direction: row;
	   flex-grow: 1;
	   align-items: center;
	   justify-content: space-between;
	   gap: 10px;
	   flex-wrap: wrap;
	   width: 100%;
   }

   .titulosIniciais {
	   display: flex;
	   font-family: 'Poppins', sans-serif;
	   flex-direction: column;
	   align-items: flex-start;
	   padding: 32px 16px 32px 16px;
	   min-width: 220px;
	   max-width: 100%;
	   flex: 1 1 320px;
	   box-sizing: border-box;
	   border-radius: 16px;
	   overflow: hidden;
	   word-break: break-word;
   }

   @media (max-width: 900px) {
	   .cabecalho-flex {
		   flex-direction: column;
		   align-items: stretch;
	   }
	   .titulosIniciais {
		   max-width: 100%;
		   padding: 24px 8px;
	   }
	   #mulher {
		   margin: 24px auto 0 auto;
		   max-width: 90vw;
		   width: 100%;
	   }
   }

   .descricao {
	   margin-top: 32px;
	   color: white;
	   font-size: 1.2rem;
	   font-weight: 400;
	   line-height: 1.5;
	   margin-left: 0;
	   display: block;
	   width: 100%;
	   box-sizing: border-box;
	   word-break: break-word;
	   overflow-wrap: break-word;
   }

   #mulher {
	   display: block;
	   width: 100%;
	   max-width: 480px;
	   height: auto;
	   object-fit: cover;
	   margin-left: auto;
	   margin-right: 16px;
	   margin-top: 0;
	   min-width: 220px;
	   min-height: 160px;
	   box-sizing: border-box;
   }

 
   @media (min-width: 700px) {
	   #mulher {
		   width: 520px;
		   max-width: 90%;
		   min-width: 320px;
		   min-height: 220px;
		   margin-right: 32px;
	   }
   }

	.tituloPopulares {
		display: flex;
		font-family: 'Poppins', sans-serif;
		font-weight: 300;
		font-size: 250%;
		margin-top: auto;
		padding-top: 50px;
		color: white;
		justify-content: center;
	}
	
	.livros_populares {
		display: flex;
		justify-content: center;
		align-items: center;
		gap: 16px;
		margin-top: -50px;
		flex-wrap: wrap;
	}

	.livros_populares img {
		display: flex;
		margin-top: 70px;
		width: 120px;
		height: auto;
		border-radius: 8px;
		box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
		object-fit: cover;
		transition: transform 0.2s;
	}

	.livros_populares img:hover {
		transform: scale(1.05);
	}

	.livros_populares_principal {
		background-color: #059a43;
		width: 100%;
		height: 500px;
	}

	.experimente-container {
		background: #2ecc71;
		padding: 4rem 1rem;
		display: flex;
		justify-content: center;
		align-items: center;
	}

	.experimente-box {
		background: rgba(255, 255, 255, 0.15);
		backdrop-filter: blur(5px);
		padding: 3rem;
		border-radius: 15px;
		text-align: center;
		max-width: 600px;
		width: 100%;
	}

	.experimente-box h2 {
		color: white;
		font-size: 2.2rem;
		margin-bottom: 2rem;
		font-weight: 600;
	}

	.experimente-btn {
		background: rgba(255, 255, 255, 0.2);
		border: 2px solid white;
		color: white;
		padding: 1.2rem 2.5rem;
		font-size: 1.1rem;
		border-radius: 50px;
		cursor: pointer;
		transition: all 0.3s ease;
		font-weight: 500;
	}

	.experimente-btn:hover {
		background: rgba(255, 255, 255, 0.3);
		transform: translateY(-3px);
	}

	
	@media (max-width: 600px) {
		.experimente-box {
			padding: 2rem 1rem;
		}
		
		.experimente-box h2 {
			font-size: 1.6rem;
		}
		
		.experimente-btn {
			padding: 1rem 2rem;
			font-size: 1rem;
		}
	}
</style>