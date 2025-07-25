<script lang="ts">
	const props = $props();
</script>
<h1 class="titulop">{props.titulo}</h1>
<h2 class="subtitulop">Conhecimento ao seu alcance, onde e quando você quiser.</h2>

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

	.titulop {
		/* importando a fonte poppins para usar no site */
		font-family: 'Poppins', sans-serif;
		font-weight: 400;
		font-style: normal;
		font-size: 400%;
	}

	.subtitulop {
		font-family: 'Poppins', sans-serif;
		font-weight: 100;
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
