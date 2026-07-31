<script lang="ts">
    import { resolve } from '$app/paths';

	type AutomationTool = {
		number: string;
		title: string;
		technologies: string[];
		description: string;
		features: string[];
		input: string;
		output: string;
	};

	const tools: AutomationTool[] = [
		{
			number: '01',
			title: 'County Setting Totals',
			technologies: ['Java', 'Gradle', 'Apache POI', 'Excel'],
			description:
				'A batch-processing application that reads county election-plan workbooks and creates a centralized, professionally formatted Excel summary.',
			features: [
				'Processes multiple Excel workbooks automatically',
				'Extracts Scan, ADA, and Print machine totals',
				'Calculates paper-roll and equipment-seal requirements',
				'Alphabetically sorts county records',
				'Creates filters, frozen headers, borders, and alternating row formatting',
				'Automatically sizes spreadsheet columns'
			],
			input: 'County election-plan Excel workbooks',
			output:
				'A consolidated Excel workbook containing county equipment and supply totals'
		},
		{
			number: '02',
			title: 'Machine Label Generator',
			technologies: ['Java', 'Gradle', 'Apache POI', 'PDF'],
			description:
				'A document-generation utility that reads machine assignments from Excel files and creates organized, printable PDF labels for equipment preparation.',
			features: [
				'Reads equipment information from county workbooks',
				'Creates labels for Scan, ADA, and Print equipment',
				'Includes county, polling location, and machine type',
				'Numbers repeated equipment assignments',
				'Handles spare machines separately',
				'Arranges labels in a consistent printable page layout'
			],
			input: 'County machine and polling-location spreadsheets',
			output: 'Printable PDF machine-label documents'
		},
		{
			number: '03',
			title: 'Setting Scheduler',
			technologies: ['Java', 'Gradle', 'Apache POI', 'iCalendar'],
			description:
				'A scheduling application that converts a shared Excel work schedule into individual calendar files that can be imported into Apple Calendar, Outlook, and other calendar applications.',
			features: [
				'Reads employee assignments from an Excel schedule',
				'Recognizes dates, counties, and custom appointment times',
				'Uses default start and end times when none are supplied',
				'Connects county assignments with addresses and administrator details',
				'Creates a separate iCalendar file for each employee',
				'Uses stable event identifiers to improve calendar re-importing'
			],
			input: 'Employee schedule and county-address Excel workbooks',
			output: 'Individual .ics calendar files for each employee'
		}
	];
</script>

<svelte:head>
	<title>Business Automation Tools | Brennen Gabriel</title>

	<meta
		name="description"
		content="Java business automation tools developed by Brennen Gabriel for spreadsheet processing, PDF label generation, and employee scheduling."
	/>
</svelte:head>

<section class="page-hero compact">
	<div class="page-shell">
		
		<a class="back-link" href={resolve('/projects')}>
			← Back to Projects
		</a>

		<p class="eyebrow">Project Collection</p>

		<h1>Business Automation Tools</h1>

		<p class="hero-text">
			Java applications designed to replace repetitive manual workflows with reliable,
			reusable automation.
		</p>

	</div>
</section>

<section class="section">
	<div class="page-shell">
		<div class="project-overview">
			<div>
				<p class="section-label">Overview</p>

				<h2>
					Turning operational spreadsheets into usable business systems.
				</h2>
			</div>

			<div class="overview-copy">
				<p>
					This collection contains three Java automation tools developed to solve
					real operational problems. Each application takes an existing manual
					process and converts it into a repeatable software workflow.
				</p>

				<p>
					The tools process Excel workbooks, calculate equipment requirements,
					generate printable PDF labels, and convert employee schedules into
					calendar events.
				</p>
			</div>
		</div>

		<div class="summary-grid">
			<div class="summary-card">
				<strong>3</strong>
				<span>Automation applications</span>
			</div>

			<div class="summary-card">
				<strong>Java</strong>
				<span>Primary language</span>
			</div>

			<div class="summary-card">
				<strong>Excel</strong>
				<span>Primary data source</span>
			</div>

			<div class="summary-card">
				<strong>PDF + ICS</strong>
				<span>Generated documents</span>
			</div>
		</div>
	</div>
</section>

<!-- {#each tools as tool}
	<section class="section tool-section">
		<div class="page-shell">
			<article class="tool-detail">
				<div class="tool-heading">
					<span class="project-number">{tool.number}</span>

					<div>
						<div class="project-meta">
							{#each tool.technologies as technology}
								<span>{technology}</span>
							{/each}
						</div>

						<h2>{tool.title}</h2>

						<p class="tool-description">
							{tool.description}
						</p>
					</div>
				</div>

				<div class="tool-layout">
					<div class="tool-content">
						<h3>Key Features</h3>

						<ul class="feature-list">
							{#each tool.features as feature}
								<li>{feature}</li>
							{/each}
						</ul>

						<div class="workflow-grid">
							<div class="workflow-card">
								<span>Input</span>
								<p>{tool.input}</p>
							</div>

							<div class="workflow-arrow" aria-hidden="true">
								→
							</div>

							<div class="workflow-card">
								<span>Output</span>
								<p>{tool.output}</p>
							</div>
						</div>
					</div>
				</div>
			</article>
		</div>
	</section>
{/each} -->

<section class="section results-section">
	<div class="page-shell">
		<div class="project-overview">
			<div>
				<p class="section-label">Business Value</p>

				<h2>
					Designed around measurable workflow improvements.
				</h2>
			</div>

			<div class="overview-copy">
				<p>
					These applications reduce the time required to manually review files,
					perform calculations, prepare documents, and enter schedule information.
				</p>

				<p>
					They also provide consistent outputs, centralized information, and
					reusable processes that can be run whenever the source information
					changes.
				</p>
			</div>
		</div>

		<div class="value-grid">
			<div class="value-card">
				<h3>Reduced Manual Entry</h3>

				<p>
					Information is extracted directly from existing spreadsheets instead
					of being retyped into separate documents.
				</p>
			</div>

			<div class="value-card">
				<h3>Consistent Output</h3>

				<p>
					Generated workbooks, labels, and calendar files follow standardized
					formats.
				</p>
			</div>

			<div class="value-card">
				<h3>Reusable Workflows</h3>

				<p>
					The applications can process updated source files without rebuilding
					the output manually.
				</p>
			</div>
		</div>
	</div>
</section>

<style>
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

	.project-overview {
		display: grid;
		grid-template-columns: minmax(0, 0.9fr) minmax(0, 1.1fr);
		gap: 4rem;
		align-items: start;
	}

	.project-overview h2 {
		max-width: 700px;
		margin: 0;
		font-size: clamp(2rem, 4vw, 3.4rem);
		line-height: 1.05;
	}

	.section-label {
		margin: 0 0 0.75rem;
		font-size: 0.78rem;
		font-weight: 800;
		letter-spacing: 0.16em;
		text-transform: uppercase;
	}

	.overview-copy {
		display: grid;
		gap: 1rem;
	}

	.overview-copy p {
		margin: 0;
		font-size: 1.05rem;
		line-height: 1.8;
	}

	.summary-grid {
		display: grid;
		grid-template-columns: repeat(4, minmax(0, 1fr));
		gap: 1rem;
		margin-top: 3rem;
	}

	.summary-card {
		display: flex;
		flex-direction: column;
		gap: 0.4rem;
		padding: 1.5rem;
		border: 1px solid rgba(127, 127, 127, 0.25);
		border-radius: 18px;
		background: rgba(127, 127, 127, 0.06);
	}

	.summary-card strong {
		font-size: 1.6rem;
	}

	.summary-card span {
		opacity: 0.72;
	}

	.tool-section {
		border-top: 1px solid rgba(127, 127, 127, 0.25);
	}

	.tool-detail {
		width: 100%;
	}

	.tool-heading {
		display: grid;
		grid-template-columns: auto minmax(0, 1fr);
		gap: 1.5rem;
		align-items: start;
	}

	.project-number {
		display: inline-flex;
		align-items: center;
		justify-content: center;
		width: 52px;
		height: 52px;
		border: 1px solid rgba(127, 127, 127, 0.35);
		border-radius: 50%;
		font-size: 0.9rem;
		font-weight: 800;
	}

	.project-meta {
		display: flex;
		flex-wrap: wrap;
		gap: 0.6rem;
	}

	.project-meta span {
		padding: 0.4rem 0.75rem;
		border: 1px solid rgba(127, 127, 127, 0.25);
		border-radius: 999px;
		font-size: 0.75rem;
		font-weight: 700;
		letter-spacing: 0.04em;
	}

	.tool-heading h2 {
		margin: 0.8rem 0 1rem;
		font-size: clamp(2rem, 4vw, 3.25rem);
		line-height: 1.1;
	}

	.tool-description {
		max-width: 850px;
		margin: 0;
		font-size: 1.08rem;
		line-height: 1.75;
	}

	.tool-layout {
		margin-top: 3rem;
	}

	.tool-content h3 {
		margin: 0;
		font-size: 1.3rem;
	}

	.feature-list {
		display: grid;
		gap: 0.75rem;
		margin: 1.25rem 0 2rem;
		padding-left: 1.25rem;
		line-height: 1.65;
	}

	.feature-list li::marker {
		font-weight: 700;
	}

	.workflow-grid {
		display: grid;
		grid-template-columns: minmax(0, 1fr) auto minmax(0, 1fr);
		gap: 1rem;
		align-items: center;
	}

	.workflow-card {
		min-height: 130px;
		padding: 1.25rem;
		border: 1px solid rgba(127, 127, 127, 0.25);
		border-radius: 16px;
		background: rgba(127, 127, 127, 0.06);
	}

	.workflow-card span {
		display: block;
		margin-bottom: 0.6rem;
		font-size: 0.75rem;
		font-weight: 800;
		letter-spacing: 0.14em;
		text-transform: uppercase;
		opacity: 0.72;
	}

	.workflow-card p {
		margin: 0;
		line-height: 1.6;
	}

	.workflow-arrow {
		font-size: 1.5rem;
		font-weight: 800;
	}


	.results-section {
		border-top: 1px solid rgba(127, 127, 127, 0.25);
	}

	.value-grid {
		display: grid;
		grid-template-columns: repeat(3, minmax(0, 1fr));
		gap: 1rem;
		margin-top: 3rem;
	}

	.value-card {
		padding: 1.5rem;
		border: 1px solid rgba(127, 127, 127, 0.25);
		border-radius: 18px;
		background: rgba(127, 127, 127, 0.06);
	}

	.value-card h3 {
		margin: 0 0 0.75rem;
	}

	.value-card p {
		margin: 0;
		line-height: 1.7;
	}

	@media (max-width: 900px) {
		.project-overview {
			grid-template-columns: 1fr;
			gap: 2rem;
		}

		.summary-grid {
			grid-template-columns: repeat(2, minmax(0, 1fr));
		}

		.value-grid {
			grid-template-columns: 1fr;
		}
	}

	@media (max-width: 600px) {
		.summary-grid,
		.workflow-grid {
			grid-template-columns: 1fr;
		}

		.workflow-arrow {
			justify-self: center;
			transform: rotate(90deg);
		}

		.tool-heading {
			grid-template-columns: 1fr;
		}

		.project-number {
			width: 46px;
			height: 46px;
		}
	}
</style>