<script>
	import { outros } from '$lib/outros';
	import { javascript } from '$lib/javascript';
    import { python } from '$lib/python';
	let frameworks = [...outros, ...javascript, ...python];
</script>

<div class="container">
	<h1 class="titulo">Um pouco sobre os Frameworks</h1>
	<div class="intro">
		<h2>O que é um Framework?</h2>
		<p class="maior">
			Framework é um conjunto de bibliotecas que abordam funcionalidades e estruturas para o
			desenvolvimento de aplicações.
		</p>
		<p class="maior">
			Ele fornece soluções para problemas comuns, permitindo a reutilização do código e otimizando o
			desenvolvimento de software.
		</p>
	</div>

	{#each frameworks as framework}
		<div class="framework-card">
			<img class="framework-image" src={framework.image} alt={framework.name} />
			<div>
				<h2 class="framework-title">{framework.name}</h2>
				<p class="framework-description">{framework.description}</p>
				<a class="framework-link" href={framework.link} target="_blank">Saiba mais</a>
			</div>
		</div>
	{/each}
</div>

<style>
	.titulo {
		text-align: center;
		margin-bottom: 20px;
		text-transform: uppercase;
	}

	.framework-card {
		display: flex;
		align-items: center;
		border: 1px solid #ddd;
		border-radius: 12px;
		padding: 16px;
		margin: 16px 0;
		box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
		transition:
			transform 0.3s,
			box-shadow 0.3s;
		background-color: #fff;
	}

	.maior {
		font-size: 20px;
	}

	.framework-card:hover {
		transform: translateY(-6px);
		box-shadow: 0 6px 12px rgba(0, 0, 0, 0.2);
	}

	.framework-image {
		width: 80px;
		height: 80px;
		margin-right: 16px;
	}

	.framework-title {
		font-size: 1.8rem;
		font-weight: bold;
		color: #34495e;
	}

	.framework-description {
		margin: 12px 0;
		color: #666;
		line-height: 1.5;
	}

	.framework-link {
		color: #196ac7;
		text-decoration: none;
		font-weight: bold;
	}

	.framework-link:hover {
		text-decoration: underline;
	}
</style>
