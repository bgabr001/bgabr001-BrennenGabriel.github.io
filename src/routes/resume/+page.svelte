<script lang="ts">
	import {base} from '$app/paths';
</script>

<svelte:head>
	<title>Resume | Brennen Gabriel</title>
	<meta
		name="description"
		content="Resume of Brennen Gabriel, Software Developer."
	/>
</svelte:head>

<section class="page-hero compact">
	<div class="page-shell">
		<p class="eyebrow">Resume</p>

		<h1>Software development, business experience, and practical projects.</h1>

		<div class="button-row">
			<a
				class="button primary"
				href={`${base}/resume/Brennen-Gabriel-Resume.pdf`}
				target="_blank"
				rel="noopener noreferrer"
			>
				Download Resume PDF
			</a>
		</div>

		<p class="small-note">
			Download the latest version of my professional resume.
		</p>
	</div>
</section>

<section class="section">
	<div class="page-shell resume-layout">

		<div class="resume-main">

			<section class="resume-section">
				<h2>Professional Summary</h2>

				<p>
					Computer Science graduate and software developer with experience
					building Java desktop applications, automation tools, web
					applications, and educational software. Passionate about solving
					real-world business problems through software engineering.
				</p>
			</section>

			<section class="resume-section">
				<h2>Featured Projects</h2>

				<div class="resume-entry">
					<h3>RMA Tracker</h3>
					<p>
						Enterprise Java desktop application featuring SQLite, PDF
						reports, Excel export, printing, automatic backups, packaging,
						and deployment.
					</p>
				</div>

				<div class="resume-entry">
					<h3>Rogue-Like Algebra</h3>
					<p>
						Educational roguelike game built with Godot and Rust to teach
						algebra through gameplay.
					</p>
				</div>

				<div class="resume-entry">
					<h3>Business Automation Tools</h3>
					<p>
						Collection of Java utilities including scheduling,
						PDF generation, spreadsheet processing,
						and election equipment management.
					</p>
				</div>
			</section>

			<section class="resume-section">
				<h2>Education</h2>

				<div class="resume-entry">
					<h3>Old Dominion University</h3>
					<p>Bachelor of Science – Computer Science</p>
				</div>

				<div class="resume-entry">
					<h3>University of Kentucky</h3>
					<p>Marketing & Economics</p>
				</div>
			</section>

		</div>

		<aside class="skills-panel">

			<h2>Technical Skills</h2>

			<div class="skill-group">
				<h3>Languages</h3>
				<p>Java, C#, C++, JavaScript, TypeScript, Rust, SQL</p>
			</div>

			<div class="skill-group">
				<h3>Frameworks & Tools</h3>
				<p>SvelteKit, Swing, Godot, Unity, Gradle, Git, GitHub</p>
			</div>

			<div class="skill-group">
				<h3>Databases</h3>
				<p>SQLite, MySQL</p>
			</div>

			<div class="skill-group">
				<h3>Other</h3>
				<p>PDF Generation, Excel Export, Application Packaging, Testing</p>
			</div>

		</aside>

	</div>
</section>