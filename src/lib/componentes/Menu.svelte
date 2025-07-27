
<script lang="ts">
	//  reutilizando o texto para diferentes pags: PROPS
	const props = $props();
</script>

<div class="primeiradiv">
  <div class="cabecalho-flex">
	<div class="titulosIniciais">
	  <h1>{props.titulo}</h1>
	  <h2>{props.subtitulo}</h2>
	  <h3 class="descricao">A Biblioteca IFRN-SGA é uma biblioteca online criada com o propósitos de democratizar o acesso à leitura, ao conhecimento e à informação. Nossa missão é conectar leitores de todas as idades a um vasto acervo digital, reunindo obras clássicas, contemporâneas, acadêmicas e independentes em um único lugar, acessível a qualquer hora e de qualquer lugar.</h3>
	</div>
	<img id="mulher" src="/retrato-jovem-mulher-lendo-um-livro.png" alt="mulher com livro">
  </div>
</div>

<!-- <div class="primeiradiv">
	<img id="mulher" src="/retrato-jovem-mulher-lendo-um-livro.png" alt="mulher com livro">

	<h1 class=>{props.titulo}</h1>
<h2 class=> Conhecimento ao seu alcance, onde e quando você quiser.</h2>
</div> -->

<div class="livros_populares_principal">
	<h3 class="tituloPopulares">Títulos Populares</h3>
	<div class="livros_populares">
		<img src="/domcasmurrolivro.jpg" alt="" />
		<img src="/pequenacoreografialivro.jpg" alt="" />
		<img src="/arianalivro.jpg" alt="" />
		<img src="/linuxlivro.jpg" alt="" />
		<img src="/anittalivro.jpeg" alt="" />
		<img src="/aguavivalivro.jpg" alt="" />
	</div>
</div>

<style>
	@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');
	html {
		font-family: 'Poppins', sans-serif;
	}
	
	.primeiradiv {
		background-color: #059a43;
		
	}

	.primeiradiv h1{
		font-weight: 1000;
		color: white;
		font-size: 100px;
		margin-left: 10%;

	}
	 
	.primeiradiv h2{
		color: white;
		margin-left: 10%;
	}

	.primeiradiv h3{
		color:  white;
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
	   overflow: visible;
	   word-break: break-word;
   }
   @media (max-width: 900px) {
	   .cabecalho-flex {
		   align-items: center;
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

   /* Responsividade para telas maiores */
   @media (min-width: 700px) {
	   #mulher {
		   width: 520px;
		   max-width: 90%;
		   min-width: 320px;
		   min-height: 220px;
		   margin-right: 32px;
	   }
   }

	.tituloPopulares{
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

	
	
	
</style>
