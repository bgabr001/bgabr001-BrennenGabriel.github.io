<script lang="ts">
	import { resolve } from '$app/paths';;
</script>

<svelte:head>
	<title>About | Brennen Gabriel</title>
</svelte:head>

<section class="page-hero compact">
	<div class="page-shell">
		<p class="eyebrow">About Me</p>
		<h1>I enjoy turning complicated tasks into clear, usable software.</h1>
	</div>
</section>

<section class="section">
	<div class="page-shell about-grid">
		<div class="about-main">
			<h2>My background</h2>
			<p>
				I am a software developer and computer science graduate from Old Dominion University.
				I also hold a degree in marketing and economics from the University of Kentucky, giving
				me a combination of technical, business, and communication skills.
			</p>
			<p>
				My projects often begin with a real workflow that can be made faster or easier. I have
				built Java desktop applications for RMA management, reporting, spreadsheet processing,
				label generation, scheduling, and data organization.
			</p>
			<p>
				I also enjoy game development and educational technology. Rogue-Like Algebra combines
				procedural gameplay with math practice to make learning more engaging.
			</p>

			<div class="button-row">
				<a class="button primary" href={resolve('/projects')}>See My Work</a>
				<a class="button secondary" href={resolve('/resume')}>View Resume</a>
			</div>
		</div>

		<aside class="profile-panel">
			<div class="profile-placeholder">BG</div>
			<h3>Brennen Gabriel</h3>
			<p>Software Developer</p>
			<ul class="detail-list">
				<li><span>Focus</span><strong>Java & Web Development</strong></li>
				<li><span>Education</span><strong>B.S. Computer Science</strong></li>
				<li><span>Location</span><strong>Lexington, Kentucky</strong></li>
			</ul>
		</aside>
	</div>
</section>

<section class="section section-alt">
	<div class="page-shell">
		<div class="section-heading">
			<p class="eyebrow">Core Strengths</p>
			<h2>How I approach development</h2>
		</div>
		<div class="card-grid three">
			<article class="info-card">
				<h3>Build for users</h3>
				<p>I focus on clear workflows, readable layouts, helpful feedback, and reliable behavior.</p>
			</article>
			<article class="info-card">
				<h3>Improve continuously</h3>
				<p>I use versioned releases, testing, documentation, and planned feature roadmaps.</p>
			</article>
			<article class="info-card">
				<h3>Finish the full product</h3>
				<p>I work beyond code to include packaging, backups, reports, exports, and deployment.</p>
			</article>
		</div>
	</div>
</section>
