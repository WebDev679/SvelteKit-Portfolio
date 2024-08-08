<script>
	import skills from '$lib/Skills';
</script>

<svelte:head>
	<title>Arnav Pratap Chaudhry — About</title>
</svelte:head>

<div class="container">
	<main>
		<h1>About</h1>
		<p>
			Hello, World! 👋 
I'm a dedicated and motivated junior at Boston University, majoring in Computer Science. Passionate about technology's potential to shape the future, I'm driven to explore diverse domains within the field.
<br>
<br>
🚀 What I'm Up To
<br>
- Exploring Machine Learning to derive meaningful insights 🤖
<br>
- Crafting seamless and user-centric digital experiences in Web Development 🌐
<br>
- Embracing efficiency and collaboration in the world of DevOps 🛠️
<br>
- Channeling curiosity into intuitive and functional Mobile App Development 📱
<br>
- Excited about the potential of Blockchain to revolutionize transparency and security 🔗
		</p>
		<h2>Skills</h2>
		{#each Object.entries(skills) as [section, technologies]}
			<ul>
				<li>
					<h4>
						{section}:
					</h4>
					<div class="list">
						{#each technologies as technology}
							<div>
								{technology}
							</div>
						{/each}
					</div>
				</li>
			</ul>
		{/each}
	</main>
</div>

<style>
	.container {
		max-width: 900px;
		padding: 0;
		display: flex;
		justify-content: center;
	}

	main {
		max-width: 100%;
		min-height: 500px;
		text-align: left;
		margin: 0 auto;
		box-sizing: border-box;
	}

	h1 {
		font-weight: 700;
		margin: 0 0 50px 0;
		font-size: 36px;
		text-align: start;
	}

	h2 {
		margin-top: 50px;
	}

	.list {
		display: flex;
		flex-direction: column;
		gap: 30px;
	}

	@media (min-width: 900px) {
		.list {
			flex-direction: row;
		}
		main > h1 {
			font-size: 48px;
		}
	}
</style>
