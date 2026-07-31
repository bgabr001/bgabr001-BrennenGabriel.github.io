<script lang="ts">
	import { asset, resolve } from '$app/paths';

	const features = [
		'Create, edit, search, and manage RMA records',
		'Track multiple repair items under one RMA',
		'Record shipping and tracking information',
		'Maintain a complete status history',
		'Generate report previews',
		'Export records to PDF and Excel',
		'Create and restore database backups',
		'Package the application for desktop deployment'
	];

	const technologies = [
		'Java',
		'Java Swing',
		'SQLite',
		'Gradle',
		'JUnit 5',
		'Apache POI',
		'PDF reporting',
		'jpackage'
	];

	const documentationLibrary = asset(
		'/documents/rmaTracker/RMA_Tracker_Documentation_Library_Master_Outline_v2.1.1.pdf'
	);

	const volumeOne = asset(
		'/documents/rmaTracker/SRS_Documentation_v2.1.1.pdf'
	);

	const volumeTwo = asset(
		'/documents/rmaTracker/Technical_Design_and_Architecture_Manual_v2.1.1.pdf'
	);

	const volumeThree = asset(
		'/documents/rmaTracker/User_Manual_and_Administgration_Guide_v2.1.1.pdf'
	);

	const volumeFour = asset(
		'/documents/rmaTracker/Installation_Deployment_Maintenance_Guide_v2.1.1.pdf'
	);
</script>

<svelte:head>
	<title>RMA Tracker | Brennen Gabriel</title>

	<meta
		name="description"
		content="RMA Tracker is a Java desktop application developed to manage repair records, equipment, shipping, reporting, and backups."
	/>
</svelte:head>

<main class="project-page">
	<section class="project-hero">
		<a class="back-link" href={resolve('/projects')}>
			← Back to Projects
		</a>

		<p class="eyebrow">Featured Project</p>

		<h1>RMA Tracker</h1>

		<p class="project-summary">
			A Java desktop application designed to manage Return Merchandise
			Authorization records, repair items, shipping information, status
			history, reports, and database backups.
		</p>

		<div class="project-actions">
			<a class="primary-button" href="#overview">
				View Project
			</a>

			<a
				class="secondary-button"
				href="https://github.com/bgabr001/RMATracker"
				target="_blank"
				rel="noreferrer"
			>
				View GitHub
			</a>
		</div>
	</section>

	<section id="overview" class="content-section">
		<p class="section-label">Overview</p>
		<h2>About the project</h2>

		<p>
			RMA Tracker was developed to provide a centralized system for managing
			the complete repair and return process. The application replaces
			disconnected spreadsheets and manual records with a structured desktop
			system backed by a SQLite database.
		</p>

		<p>
			Each RMA can contain multiple repair items, shipping records, tracking
			numbers, notes, status updates, and historical information. Users can
			search records, preview reports, export data, and maintain database
			backups from within the application.
		</p>
	</section>

	<section class="content-section">
		<p class="section-label">Problem</p>
		<h2>The problem it solves</h2>

		<p>
			Repair records can become difficult to manage when customer details,
			equipment information, tracking numbers, repair notes, and status
			updates are stored in separate files.
		</p>

		<p>
			RMA Tracker brings this information into one application and creates a
			consistent workflow for recording, searching, updating, reporting, and
			archiving repair activity.
		</p>
	</section>

	<section class="content-section">
		<p class="section-label">Capabilities</p>
		<h2>Key features</h2>

		<div class="card-grid">
			{#each features as feature (feature)}
				<article class="info-card">
					<p>{feature}</p>
				</article>
			{/each}
		</div>
	</section>

	<section class="content-section">
		<p class="section-label">Technology</p>
		<h2>Technology stack</h2>

		<div class="tag-list">
			{#each technologies as technology (technology)}
				<span class="technology-tag">{technology}</span>
			{/each}
		</div>
	</section>

	<section class="content-section">
		<p class="section-label">Architecture</p>
		<h2>Application structure</h2>

		<div class="architecture-grid">
			<article class="architecture-card">
				<h3>User interface</h3>
				<p>
					Java Swing windows, forms, dialogs, tables, report previews,
					menus, and user confirmations.
				</p>
			</article>

			<article class="architecture-card">
				<h3>Business logic</h3>
				<p>
					Service classes handle searching, backups, validation, report
					generation, and application workflows.
				</p>
			</article>

			<article class="architecture-card">
				<h3>Data access</h3>
				<p>
					Repository classes manage database queries, RMA records,
					repair items, shipping information, and status history.
				</p>
			</article>

			<article class="architecture-card">
				<h3>Database</h3>
				<p>
					SQLite provides local persistent storage without requiring a
					separate database server.
				</p>
			</article>
		</div>
	</section>

	<section class="content-section">
		<p class="section-label">Development</p>
		<h2>My contribution</h2>

		<p>
			I designed and developed the application, database structure, desktop
			interface, search system, reporting tools, export features, backup
			workflow, automated tests, and desktop packaging process.
		</p>

		<p>
			I also created formal software documentation covering the application’s
			requirements, technical architecture, user instructions, installation,
			deployment, and maintenance.
		</p>
	</section>

	<section class="content-section">
	<p class="section-label">Documentation</p>
	<h2>Engineering documentation</h2>

	<p>
		RMA Tracker includes a professional documentation library covering
		software requirements, architecture, user guidance, installation,
		deployment, and long-term maintenance.
	</p>

	<div class="documentation-grid">
		<article class="documentation-card featured-document">
			<div class="document-heading">
				<span class="document-volume">Overview</span>
				<span class="document-status available">Available</span>
			</div>

			<h3>RMA Tracker Documentation Library</h3>

			<p>
				An overview of the complete four-volume documentation set,
				including the purpose, scope, planned content, and estimated
				length of each volume.
			</p>

			<div class="document-meta">
				<span>PDF</span>
				<span>Four volumes</span>
				<span>Documentation roadmap</span>
			</div>

			<div class="document-actions">
				<a
					class="primary-button"
					href={documentationLibrary}
					target="_blank"
					rel="noreferrer"
				>
					View PDF
				</a>

				<a
					class="secondary-button"
					href={documentationLibrary}
					download
				>
					Download PDF
				</a>
			</div>
		</article>

		<article class="documentation-card featured-document">
			<div class="document-heading">
				<span class="document-volume">Volume I</span>
				<span class="document-status available">Available</span>
			</div>

			<h3>Software Requirements Specification</h3>

			<p>
				Defines the functional and nonfunctional requirements,
				external interfaces, data requirements, business rules,
				use cases, acceptance criteria, and future enhancements for
				RMA Tracker Version 2.1.1.
			</p>

			<div class="document-meta">
				<span>PDF</span>
				<span>50 pages</span>
				<span>Version 2.1.1</span>
			</div>

			<div class="document-actions">
				<a
					class="primary-button"
					href={volumeOne}
					target="_blank"
					rel="noreferrer"
				>
					View PDF
				</a>

				<a
					class="secondary-button"
					href={volumeOne}
					download
				>
					Download PDF
				</a>
			</div>
		</article>

		<article class="documentation-card featured-document">
			<div class="document-heading">
				<span class="document-volume">Volume II</span>
				<span class="document-status available">Available</span>
			</div>

			<h3>Technical Design & Architecture Manual</h3>

			<p>
				Provides a comprehensive technical reference for the application
				architecture, project structure, technology stack, database design,
				class organization, user interface, reporting system, backup and
				recovery, packaging, testing, security, reliability, performance,
				and future architecture of RMA Tracker Version 2.1.1.
			</p>

			<div class="document-actions">
				<a
					class="primary-button"
					href={volumeTwo}
					target="_blank"
					rel="noreferrer"
				>
					View PDF
				</a>

				<a
					class="secondary-button"
					href={volumeTwo}
					download
				>
					Download PDF
				</a>
			</div>

		</article>

		<article class="documentation-card featured-document">
			<div class="document-heading">
				<span class="document-volume">Volume III</span>
				<span class="document-status available">Available</span>
			</div>

			<h3>User Manual & Administration Guide</h3>

			<p>
				Provides end-user and administrator instructions for creating
				RMAs, managing repair items, searching, reporting, exporting,
				backing up, restoring, and troubleshooting.
			</p>

			<div class="document-actions">
				<a
					class="primary-button"
					href={volumeThree}
					target="_blank"
					rel="noreferrer"
				>
					View PDF
				</a>

				<a
					class="secondary-button"
					href={volumeThree}
					download
				>
					Download PDF
				</a>
			</div>
		</article>

		<article class="documentation-card featured-document>">
			<div class="document-heading">
				<span class="document-volume">Volume IV</span>
				<span class="document-status available">Available</span>
			</div>

			<h3>Installation, Deployment & Maintenance Guide</h3>

			<p>
				Covers installation, building, packaging, distribution,
				software updates, backup and recovery, maintenance, and
				release procedures.
			</p>

			<div class="document-actions">
				<a
					class="primary-button"
					href={volumeFour}
					target="_blank"
					rel="noreferrer"
				>
					View PDF
				</a>

				<a
					class="secondary-button"
					href={volumeFour}
					download
				>
					Download PDF
				</a>
			</div>
		</article>
	</div>
</section>
	
	<section class="content-section">
		<p class="section-label">Roadmap</p>
		<h2>Future development</h2>

		<ul class="roadmap-list">
			<li>User accounts and permissions</li>
			<li>Cloud synchronization</li>
			<li>Automatic carrier tracking updates</li>
			<li>Management dashboard and analytics</li>
			<li>Customer portal</li>
			<li>Integration with the WarpTech Service Platform</li>
		</ul>
	</section>
</main>

<style>
	.project-page {
		width: min(1120px, calc(100% - 2rem));
		margin: 0 auto;
		padding: 4rem 0 6rem;
	}

	.project-hero {
		position: relative;
		padding: 3rem 0 5rem;
	}

	.project-hero::before {
		position: absolute;
		top: -180px;
		right: -260px;
		z-index: -1;
		width: 650px;
		height: 650px;
		border-radius: 50%;
		background: rgba(54, 191, 244, 0.12);
		filter: blur(90px);
		content: "";
	}

	.back-link {
		display: inline-block;
		margin-bottom: 3rem;
		color: var(--muted);
		text-decoration: none;
		transition: color 0.2s ease;
	}

	.back-link:hover {
		color: var(--accent);
	}

	.eyebrow,
	.section-label {
		margin: 0 0 0.75rem;
		color: var(--accent);
		font-size: 0.8rem;
		font-weight: 800;
		letter-spacing: 0.14em;
		text-transform: uppercase;
	}

	h1 {
		max-width: 900px;
		margin: 0;
		color: var(--text);
		font-size: clamp(3rem, 9vw, 6rem);
		line-height: 0.95;
		letter-spacing: -0.06em;
	}

	.project-summary {
		max-width: 760px;
		margin: 2rem 0 0;
		color: var(--muted);
		font-size: clamp(1.1rem, 2vw, 1.35rem);
		line-height: 1.7;
	}

	.project-actions {
		display: flex;
		flex-wrap: wrap;
		gap: 1rem;
		margin-top: 2.5rem;
	}

	.primary-button,
	.secondary-button {
		display: inline-flex;
		align-items: center;
		justify-content: center;
		min-height: 48px;
		padding: 0.75rem 1.25rem;
		border-radius: 0.7rem;
		font-weight: 750;
		text-decoration: none;
		transition:
			transform 0.2s ease,
			background 0.2s ease,
			border-color 0.2s ease,
			color 0.2s ease;
	}

	.primary-button {
		border: 1px solid transparent;
		background: var(--accent);
		color: #03111c;
	}

	.primary-button:hover {
		transform: translateY(-2px);
		background: #91e2ff;
	}

	.secondary-button {
		border: 1px solid var(--line);
		background: rgba(255, 255, 255, 0.03);
		color: var(--text);
	}

	.secondary-button:hover {
		transform: translateY(-2px);
		border-color: rgba(101, 212, 255, 0.4);
		color: var(--accent);
	}

	.content-section {
		padding: 5rem 0;
		border-top: 1px solid var(--line);
	}

	.content-section h2 {
		margin: 0 0 1.5rem;
		color: var(--text);
		font-size: clamp(2rem, 5vw, 3.5rem);
		letter-spacing: -0.04em;
	}

	.content-section > p:not(.section-label) {
		max-width: 780px;
		color: var(--muted);
		font-size: 1.05rem;
		line-height: 1.8;
	}

	.card-grid,
	.architecture-grid {
		display: grid;
		grid-template-columns: repeat(2, minmax(0, 1fr));
		gap: 1rem;
		margin-top: 2rem;
	}

	.info-card,
	.architecture-card {
		padding: 1.5rem;
		border: 1px solid var(--line);
		border-radius: var(--radius);
		background: var(--panel);
		box-shadow: 0 18px 60px rgba(0, 0, 0, 0.12);
	}

	.info-card p {
		margin: 0;
		color: var(--muted);
		line-height: 1.6;
	}

	.architecture-card h3 {
		margin: 0 0 0.75rem;
		color: var(--text);
	}

	.architecture-card p {
		margin: 0;
		color: var(--muted);
		line-height: 1.7;
	}

	.tag-list {
		display: flex;
		flex-wrap: wrap;
		gap: 0.75rem;
		margin-top: 2rem;
	}

	.technology-tag {
		padding: 0.6rem 0.9rem;
		border: 1px solid rgba(101, 212, 255, 0.18);
		border-radius: 999px;
		background: rgba(101, 212, 255, 0.07);
		color: var(--accent);
		font-size: 0.9rem;
		font-weight: 700;
	}

	.roadmap-list {
		display: grid;
		gap: 1rem;
		max-width: 780px;
		padding-left: 1.25rem;
		color: var(--muted);
		line-height: 1.6;
	}

	.roadmap-list li::marker {
		color: var(--accent);
	}

	@media (max-width: 700px) {
		.project-page {
			padding-top: 2rem;
		}

		.project-hero {
			padding-bottom: 3rem;
		}

		.card-grid,
		.architecture-grid,
		.documentation-grid {
			grid-template-columns: 1fr;
		}
	}


	.documentation-grid {
	display: grid;
	grid-template-columns: repeat(2, minmax(0, 1fr));
	gap: 1rem;
	margin-top: 2rem;
}

.documentation-card {
	display: flex;
	flex-direction: column;
	padding: 1.75rem;
	border: 1px solid var(--line);
	border-radius: var(--radius);
	background: var(--panel);
	box-shadow: 0 18px 60px rgba(0, 0, 0, 0.12);
}

.featured-document {
	border-color: rgba(101, 212, 255, 0.35);
	background: linear-gradient(
		145deg,
		rgba(23, 55, 80, 0.9),
		rgba(13, 27, 47, 0.9)
	);
}

.document-heading {
	display: flex;
	align-items: center;
	justify-content: space-between;
	gap: 1rem;
	margin-bottom: 1.25rem;
}

.document-volume {
	color: var(--accent);
	font-size: 0.8rem;
	font-weight: 800;
	letter-spacing: 0.12em;
	text-transform: uppercase;
}

.document-status {
	display: inline-flex;
	padding: 0.35rem 0.65rem;
	border: 1px solid var(--line);
	border-radius: 999px;
	color: var(--muted);
	font-size: 0.75rem;
	font-weight: 700;
}

.document-status.available {
	border-color: rgba(101, 212, 255, 0.25);
	background: rgba(101, 212, 255, 0.07);
	color: var(--accent);
}

.documentation-card h3 {
	margin: 0 0 0.85rem;
	color: var(--text);
	font-size: 1.35rem;
}

.documentation-card p {
	margin: 0;
	color: var(--muted);
	line-height: 1.7;
}

.document-meta {
	display: flex;
	flex-wrap: wrap;
	gap: 0.5rem;
	margin-top: 1.5rem;
}

.document-meta span {
	padding: 0.35rem 0.65rem;
	border: 1px solid rgba(101, 212, 255, 0.18);
	border-radius: 999px;
	background: rgba(101, 212, 255, 0.07);
	color: var(--accent);
	font-size: 0.75rem;
	font-weight: 700;
}

.document-actions {
	display: flex;
	flex-wrap: wrap;
	gap: 0.75rem;
	margin-top: auto;
	padding-top: 1.75rem;
}

.planned-document {
	opacity: 0.72;
}
</style>