<script lang="ts">
	import { base } from '$app/paths';
</script>

<svelte:head>
	<title>Resume | Brennen Gabriel</title>
</svelte:head>

<section class="page-hero compact">
	<div class="page-shell">
		<p class="eyebrow">Resume</p>
		<h1>Software development, business experience, and practical projects.</h1>
		<div class="button-row">
			<a class="button primary" href={`${base}/resume/Brennen-Gabriel-Resume.pdf`} target="_blank">
				Download Resume PDF
			</a>
		</div>
		<p class="small-note">
			Place your PDF at <code>static/resume/Brennen-Gabriel-Resume.pdf</code>.
		</p>
	</div>
</section>

<section class="section">
	<div class="page-shell resume-layout">
		<div class="resume-main">
			<section class="resume-section">
				<h2>Summary</h2>
				<p>
					Computer science graduate and software developer with experience building Java desktop
					applications, automation tools, websites, and games. Skilled in taking projects from
					requirements and implementation through testing, documentation, packaging, and release.
				</p>
			</section>

			<section class="resume-section">
				<h2>Selected Projects</h2>
				<div class="resume-entry">
					<h3>RMA Tracker</h3>
					<p>Java, Swing, SQLite, Gradle, PDF and Excel exports</p>
				</div>
				<div class="resume-entry">
					<h3>Rogue-Like Algebra</h3>
					<p>Godot, Rust, procedural math generation, educational game design</p>
				</div>
				<div class="resume-entry">
					<h3>Business Automation Utilities</h3>
					<p>Java, Apache POI, PDF generation, iCalendar processing</p>
				</div>
			</section>

			<section class="resume-section">
				<h2>Education</h2>
				<div class="resume-entry">
					<h3>Old Dominion University</h3>
					<p>Bachelor of Science in Computer Science · 2025</p>
				</div>
				<div class="resume-entry">
					<h3>University of Kentucky</h3>
					<p>Marketing and Economics · 2016</p>
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
				<h3>Data & Reporting</h3>
				<p>SQLite, Apache POI, Excel, PDF generation, iCalendar</p>
			</div>
			<div class="skill-group">
				<h3>Development</h3>
				<p>Testing, debugging, documentation, application packaging</p>
			</div>
		</aside>
	</div>
</section>
