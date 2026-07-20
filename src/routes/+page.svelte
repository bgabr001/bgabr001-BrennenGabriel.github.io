<script lang="ts">
	import { resolve } from '$app/paths';
	
	const codeExample = `developer = {
	name: "Brennen Gabriel",
	specialty: "Java & Web",
	building: "Useful software",
	status: "Open to opportunities"
};`;
</script>

<svelte:head>
	<title>Brennen Gabriel | Software Developer</title>
	<meta
		name="description"
		content="Brennen Gabriel's software development portfolio featuring Java applications, web development, automation tools, and educational games."
	/>
</svelte:head>

<section class="hero">
	<div class="page-shell hero-grid">
		<div class="hero-copy">
			<p class="eyebrow">Software Developer · Problem Solver · Builder</p>

			<h1>Building practical software that solves real problems.</h1>

			<p class="hero-text">
				I am Brennen Gabriel, a computer science graduate and software developer focused on
				Java applications, desktop tools, web development, and educational games.
			</p>

			<div class="button-row">
				<a class="button primary" href={resolve('/projects')}>
					View My Projects
				</a>

				<a class="button secondary" href={resolve('/contact')}>
					Contact Me
				</a>
			</div>
		</div>

		<div class="hero-card">
			<div class="code-window">
				<div class="window-dots" aria-hidden="true">
					<span></span>
					<span></span>
					<span></span>
				</div>

				<pre><code><span class="code-muted">// Current focus</span>
{codeExample}</code></pre>
			</div>
		</div>
	</div>
</section>

<section class="section">
	<div class="page-shell">
		<div class="section-heading">
			<p class="eyebrow">Featured Work</p>

			<h2>Projects with a real purpose</h2>

			<p>
				Selected applications that demonstrate software design, problem-solving, and
				usability.
			</p>
		</div>

		<div class="card-grid three">
			<article class="project-card featured">
				<span class="project-tag">Java Desktop Application</span>

				<h3>RMA Tracker</h3>

				<p>
					A complete return-material authorization tracking system with reports, exports,
					backups, search, status history, and packaged desktop releases.
				</p>

				<a class="text-link" href={resolve('/projects')}/#rma-tracker>
					Explore project →
				</a>
			</article>

			<article class="project-card">
				<span class="project-tag">Godot · Rust</span>

				<h3>Rogue-Like Algebra</h3>

				<p>
					An educational rogue-like game that combines turn-based combat with adaptive
					algebra challenges for middle and high school students.
				</p>

				<a class="text-link" href={resolve('/projects')}/#rogue-like-algebra>
					Explore project →
				</a>
			</article>

			<article class="project-card">
				<span class="project-tag">Java · Apache POI</span>

				<h3>Automation Tools</h3>

				<p>
					Business utilities for scheduling, machine labels, county totals, and other
					repetitive workflows.
				</p>

				<a class="text-link" href={resolve('/projects')}/#automation-tools>
					Explore project →
				</a>
			</article>
		</div>
	</div>
</section>

<section class="section section-alt">
	<div class="page-shell stats-grid">
		<div>
			<p class="eyebrow">What I Work With</p>

			<h2>A practical, full-project skill set</h2>
		</div>

		<div class="stat-card">
			<strong>Java</strong>
			<span>Desktop applications, Gradle, SQLite, testing</span>
		</div>

		<div class="stat-card">
			<strong>Web</strong>
			<span>SvelteKit, HTML, CSS, JavaScript, GitHub Pages</span>
		</div>

		<div class="stat-card">
			<strong>Games</strong>
			<span>Godot, Rust, Unity, C#</span>
		</div>
	</div>
</section>