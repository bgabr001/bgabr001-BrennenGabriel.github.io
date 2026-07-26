<script lang="ts">
	import { resolve } from '$app/paths';
</script>

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
					<span>Java</span><span>JavaSwing</span><span>SQLite</span><span>Gradle</span>
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
				<a class="text-link" href={resolve('/projects/rma-tracker')}>
					View RMA Tracker →
				</a>
			</div>
		</article>

		<article class="project-detail" id="automation-tools">
			<div class="project-number">02</div>
		<div>
			<div class="project-meta">
				<span>Java</span><span>Apache POI</span><span>PDF</span><span>iCalendar</span>
			</div>

			<h2>Business Automation Tools</h2>

			<p>
				A collection of Java applications developed to automate repetitive business workflows,
				reduce manual effort, and improve operational efficiency. Each tool was created to solve
				real-world business challenges through automation and data processing.
			</p>

			<div class="mini-project-grid">
				<div>
					<h3>Setting Scheduler</h3>
					<p>
						Reads Excel schedules and automatically generates individual iCalendar (.ics) files
						for employees, eliminating manual calendar creation.
					</p>
				</div>

				<div>
					<h3>Machine Label Generator</h3>
					<p>
						Generates organized, print-ready PDF labels for election equipment using county
						planning data, improving deployment accuracy and consistency.
					</p>
				</div>

				<div>
					<h3>Billing &amp; County Reporting</h3>
					<p>
						Processes county inventory spreadsheets to calculate billable machine totals,
						aggregate county statistics, and generate formatted reports used for billing and
						operational planning.
					</p>
				</div>
			</div>
		</div>
	</article>

		<article class="project-detail" id="portfolio-website">
			<div class="project-number">03</div>
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
