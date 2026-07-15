<svelte:head>
	<title>Brennen Gabriel | Software Developer</title>
	<meta
		name="description"
		content="Portfolio website for Brennen Gabriel, a software developer."
	/>
</svelte:head>

<script lang="ts">
	const projects = [
		{
			name: 'RMA Tracker',
			description: 'A Java Swing and SQLite desktop application for managing RMAs.'
		},
		{
			name: 'Rogue-Like Algebra',
			description: 'An educational roguelike game that teaches algebra through combat.'
		},
		{
			name: 'Setting Scheduler',
			description: 'A Java application that converts Excel schedules into calendar files.'
		}
	];
</script>

<header>
	<nav>
		<a href="#home">Home</a>
		<a href="#about">About</a>
		<a href="#projects">Projects</a>
		<a href="#contact">Contact</a>
	</nav>
</header>

<main>
	<section id="home" class="hero">
		<p class="eyebrow">Software Developer</p>
		<h1>Brennen Gabriel</h1>
		<p>
			I build practical desktop applications, websites, developer tools,
			and educational games.
		</p>

		<a class="button" href="#projects">View my projects</a>
	</section>

	<section id="about">
		<h2>About Me</h2>
		<p>
			I am a computer science graduate with experience building Java,
			Svelte, Rust, Godot, and database-driven applications.
		</p>
	</section>

	<section id="projects">
		<h2>Projects</h2>

		<div class="project-grid">
			{#each projects as project}
				<article>
					<h3>{project.name}</h3>
					<p>{project.description}</p>
				</article>
			{/each}
		</div>
	</section>

	<section id="contact">
		<h2>Contact</h2>
		<p>
			Visit my
			<a href="https://github.com/bgabr001">GitHub profile</a>.
		</p>
	</section>
</main>

<footer>
	<p>© {new Date().getFullYear()} Brennen Gabriel</p>
</footer>

<style>
	:global(*) {
		box-sizing: border-box;
	}

	:global(html) {
		scroll-behavior: smooth;
	}

	:global(body) {
		margin: 0;
		background: #0f172a;
		color: #e2e8f0;
		font-family:
			Inter, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI",
			sans-serif;
		line-height: 1.6;
	}

	header {
		position: sticky;
		top: 0;
		background: rgb(15 23 42 / 90%);
		backdrop-filter: blur(12px);
		border-bottom: 1px solid #1e293b;
	}

	nav {
		display: flex;
		justify-content: flex-end;
		gap: 1.5rem;
		max-width: 1100px;
		margin: auto;
		padding: 1rem 1.5rem;
	}

	a {
		color: #7dd3fc;
		text-decoration: none;
	}

	a:hover {
		color: white;
	}

	main {
		max-width: 1100px;
		margin: auto;
		padding: 0 1.5rem;
	}

	section {
		padding: 5rem 0;
	}

	.hero {
		min-height: 80vh;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: flex-start;
	}

	.eyebrow {
		color: #38bdf8;
		font-weight: 700;
		text-transform: uppercase;
		letter-spacing: 0.15em;
	}

	h1 {
		margin: 0;
		font-size: clamp(3rem, 10vw, 6rem);
		line-height: 1;
	}

	h2 {
		font-size: 2rem;
	}

	.button {
		display: inline-block;
		margin-top: 1rem;
		padding: 0.8rem 1.25rem;
		background: #0284c7;
		color: white;
		border-radius: 0.5rem;
		font-weight: 700;
	}

	.project-grid {
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
		gap: 1rem;
	}

	article {
		padding: 1.5rem;
		background: #1e293b;
		border: 1px solid #334155;
		border-radius: 0.75rem;
	}

	article h3 {
		margin-top: 0;
	}

	footer {
		padding: 2rem;
		text-align: center;
		border-top: 1px solid #1e293b;
	}
</style>