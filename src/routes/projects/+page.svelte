<svelte:head>
	<title>Projects | Brennen Gabriel</title>
</svelte:head>

<section class="page-hero compact">
	<div class="page-shell">
		<p class="eyebrow">Projects</p>
		<h1>Software built to solve practical problems.</h1>
		<p class="hero-text">
			A selection of desktop applications, automation tools, games, and web projects.
		</p>
	</div>
</section>

<section class="section">
	<div class="page-shell project-list">
		<article class="project-detail" id="rma-tracker">
			<div class="project-number">01</div>
			<div>
				<div class="project-meta">
					<span>Java</span><span>Swing</span><span>SQLite</span><span>Gradle</span>
				</div>
				<h2>RMA Tracker</h2>
				<p>
					A desktop application for managing return-material authorizations and every machine
					associated with each record. The system is designed as a complete business tool rather
					than a simple class project.
				</p>
				<ul class="feature-list">
					<li>Create, edit, search, and filter RMA records</li>
					<li>Track machines, shipping details, and status history</li>
					<li>Generate printable reports and print previews</li>
					<li>Export selected and filtered data to PDF and Excel</li>
					<li>Create automatic database backups</li>
					<li>Package versioned macOS application releases</li>
				</ul>
				<p class="project-note">Add screenshots, documentation links, and downloads here later.</p>
			</div>
		</article>

		<article class="project-detail" id="rogue-like-algebra">
			<div class="project-number">02</div>
			<div>
				<div class="project-meta">
					<span>Godot</span><span>Rust</span><span>Game Design</span>
				</div>
				<h2>Rogue-Like Algebra</h2>
				<p>
					An educational turn-based rogue-like designed to help students practice algebra.
					Players answer generated math questions during combat, with difficulty and challenge
					types changing as they progress.
				</p>
				<ul class="feature-list">
					<li>Procedurally generated algebra questions</li>
					<li>Linear, quadratic, and inequality problem types</li>
					<li>Turn-based combat and enemy behavior</li>
					<li>Difficulty levels and non-repeating questions</li>
					<li>Godot game interface powered by Rust modules</li>
				</ul>
			</div>
		</article>

		<article class="project-detail" id="automation-tools">
			<div class="project-number">03</div>
			<div>
				<div class="project-meta">
					<span>Java</span><span>Apache POI</span><span>PDF</span><span>iCalendar</span>
				</div>
				<h2>Business Automation Tools</h2>
				<p>
					A group of Java utilities that replace repetitive manual processes with repeatable,
					consistent workflows.
				</p>
				<div class="mini-project-grid">
					<div>
						<h3>Setting Scheduler</h3>
						<p>Reads Excel schedules and creates individual iCalendar files.</p>
					</div>
					<div>
						<h3>Machine Label Generator</h3>
						<p>Creates organized, print-ready PDF labels from election planning data.</p>
					</div>
					<div>
						<h3>County Setting Totals</h3>
						<p>Processes county spreadsheets and generates a consolidated totals workbook.</p>
					</div>
					<div>
						<h3>Machine Billing Count</h3>
						<p>Calculates machine counts for business reporting and billing workflows.</p>
					</div>
				</div>
			</div>
		</article>

		<article class="project-detail">
			<div class="project-number">04</div>
			<div>
				<div class="project-meta">
					<span>SvelteKit</span><span>CSS</span><span>GitHub Pages</span>
				</div>
				<h2>Portfolio Website</h2>
				<p>
					This responsive multi-page portfolio was designed to present projects, technical
					experience, documentation, and professional information in a clear structure.
				</p>
			</div>
		</article>
	</div>
</section>
