<script lang="ts">
	import { asset } from '$app/paths';

	const documentationLibrary = asset(
		'/documents/rmaTracker/RMA_Tracker_Documentation_Outline_Volumes_I-IV.pdf'
	);

	const volumeOne = asset(
		'/documents/rmaTracker/SRS_Documentation_v2.1.1.pdf'
	);
</script>

<svelte:head>
	<title>Documentation | Brennen Gabriel</title>
	<meta
		name="description"
		content="Professional software engineering documentation for Brennen Gabriel's projects."
	/>
</svelte:head>

<section class="page-hero compact">
	<div class="page-shell">
		<p class="eyebrow">Documentation</p>
		<h1>Software engineering documentation.</h1>
		<p class="hero-text">
			Requirements, architecture, user guidance, and deployment documentation created for
			my software projects.
		</p>
	</div>
</section>

<section class="section">
	<div class="page-shell">
		<div class="documentation-header">
			<div>
				<p class="eyebrow">RMA Tracker</p>
				<h2>Documentation Library</h2>
				<p>
					A professional four-volume documentation set covering the complete software
					development lifecycle of RMA Tracker Version 2.1.1.
				</p>
			</div>
		</div>

		<div class="documentation-grid">
			<article class="documentation-card">
				<div class="document-number">Overview</div>

				<div>
					<p class="document-type">Documentation Library</p>
					<h3>RMA Tracker Documentation Outline</h3>

					<p>
						An overview of the four-volume documentation library, including the purpose,
						scope, and planned content of each volume.
					</p>

					<div class="document-meta">
						<span>PDF</span>
						<span>4 Volumes</span>
						<span>Project Overview</span>
					</div>

					<div class="document-actions">
						<a
							class="button primary"
							href={documentationLibrary}
							target="_blank"
							rel="noreferrer"
						>
							View PDF
						</a>

						<a class="button secondary" href={documentationLibrary} download>
							Download
						</a>
					</div>
				</div>
			</article>

			<article class="documentation-card">
				<div class="document-number">Volume I</div>

				<div>
					<p class="document-type">Software Requirements Specification</p>
					<h3>RMA Tracker Version 2.1.1 SRS</h3>

					<p>
						Defines the application's functional requirements, nonfunctional requirements,
						interfaces, data requirements, business rules, use cases, and acceptance
						criteria.
					</p>

					<div class="document-meta">
						<span>PDF</span>
						<span>50 Pages</span>
						<span>Version 2.1.1</span>
					</div>

					<div class="document-actions">
						<a
							class="button primary"
							href={volumeOne}
							target="_blank"
							rel="noreferrer"
						>
							View PDF
						</a>

						<a class="button secondary" href={volumeOne} download>
							Download
						</a>
					</div>
				</div>
			</article>

			<article class="documentation-card upcoming">
				<div class="document-number">Volume II</div>

				<div>
					<p class="document-type">Technical Design & Architecture</p>
					<h3>Architecture Manual</h3>

					<p>
						Documents the project structure, database design, software architecture,
						classes, reporting system, backup system, packaging, and testing strategy.
					</p>

					<div class="document-status">In Progress</div>
				</div>
			</article>

			<article class="documentation-card upcoming">
				<div class="document-number">Volume III</div>

				<div>
					<p class="document-type">User Manual</p>
					<h3>User & Administration Guide</h3>

					<p>
						Provides instructions for creating RMAs, managing repair items, searching,
						reporting, exporting, backing up, restoring, and troubleshooting.
					</p>

					<div class="document-status">Planned</div>
				</div>
			</article>

			<article class="documentation-card upcoming">
				<div class="document-number">Volume IV</div>

				<div>
					<p class="document-type">Deployment & Maintenance</p>
					<h3>Installation and Maintenance Guide</h3>

					<p>
						Covers installation, building, packaging, distribution, updating, backup,
						recovery, maintenance, and release procedures.
					</p>

					<div class="document-status">Planned</div>
				</div>
			</article>
		</div>
	</div>
</section>