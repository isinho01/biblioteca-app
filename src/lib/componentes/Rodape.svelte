<footer>
	<p class="if">
		<a href="/">
			<img
				class="logo"
				src="/Campus São Gonçalo do Amarante - Logo_Negat Hor.png"
				alt="Logo do campus"
			/>
		</a>
	</p>

	<br />
	<p class="copy">@Copyright 2025 IFRN Campus SGA</p>
</footer>

<style>
	@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');
	footer {
		position: fixed;
		bottom: 0;
		width: 100%;
		background-color: #093800;
		color: rgb(255, 255, 255);
		align-items: center;
		padding: 10px 0;
	}
   .if {
	   max-width: 200px;
	   width: 100%;
	   height: auto; /* Mantém proporção */
	   flex: 1; /* Ocupa espaço disponível */
	   min-width: 150px;
	   position: relative;
	   top: 20px;
	}

	.copy {
		font-style: italic;
		display: flex;
		justify-content: right;
	}

	@media (max-width: 600px) {
		.if {
			margin: 0 auto; /* Centraliza logo */
		}
	}
</style>
