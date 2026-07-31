<script lang="ts">
	import { resolve } from '$app/paths';

	type AutomationTool = {
		number: string;
		title: string;
		github: string;
		technologies: string[];
		summary: string;
		problem: string[];
		workflow: string[];
		implementation: string[];
		features: string[];
		input: string;
		output: string;
		impact: string;
	};

	const tools: AutomationTool[] = [
		{
			number: '01',
			title: 'County Setting Totals',
			github: 'https://github.com/bgabr001/CountySettingMachineTotals.git',
			technologies: ['Java', 'Gradle', 'Apache POI', 'Excel'],
			summary:
				'County Setting Totals is a batch-processing application that reviews a collection of county election-plan workbooks and produces one consolidated Excel report containing equipment and supply totals.',
			problem: [
				'Operational information was distributed across many separate county spreadsheets. Producing an overall summary required opening each workbook, locating the appropriate values, recording the totals, and then checking the results manually.',
				'That process was slow and vulnerable to transcription errors, inconsistent formatting, overlooked files, and calculation mistakes. It also had to be repeated whenever one of the source workbooks changed.',
				'The application replaces that manual review process with a repeatable workflow that reads every supported workbook, extracts the required values, and prepares a standardized report automatically.'
			],
			workflow: [
				'The program scans a designated input directory and identifies the county election-plan workbooks that need to be processed.',
				'Apache POI opens each Excel file and reads the cells that contain machine quantities, supply requirements, and other operational totals.',
				'The extracted information is normalized into a consistent internal structure so that differences in file order do not affect the final report.',
				'County records are sorted alphabetically and written to a new summary workbook, with one row representing each county.',
				'The final workbook is formatted with a professional header, alternating row shading, borders, filters, frozen header rows, and automatically sized columns.'
			],
			implementation: [
				'Java provides the file-processing and business-logic layer, while Gradle manages the project build and the Apache POI dependency.',
				'The program separates workbook discovery, data extraction, calculation, sorting, and report generation into distinct processing stages.',
				'Workbook resources are opened and closed safely so that large batches can be processed without leaving files locked or consuming unnecessary memory.',
				'The generated workbook is designed to be immediately usable by staff without requiring additional cleanup or manual formatting.'
			],
			features: [
				'Processes many county Excel workbooks in one run',
				'Extracts Scan, ADA, and Print machine totals',
				'Calculates paper-roll and equipment-seal requirements',
				'Alphabetically sorts county records',
				'Applies filters, frozen headers, borders, and alternating row formatting',
				'Automatically sizes spreadsheet columns'
			],
			input: 'A directory containing county election-plan Excel workbooks.',
			output:
				'A consolidated Excel workbook containing organized county equipment and supply totals.',
			impact:
				'The application turns a repetitive multi-file review task into a single automated operation. It reduces manual entry, improves consistency, makes updated reports easier to regenerate, and gives staff a centralized source for planning and verification.'
		},
		{
			number: '02',
			title: 'Machine Label Generator',
			github: 'https://github.com/bgabr001/SettingScheduler.git',
			technologies: ['Java', 'Gradle', 'Apache POI', 'PDF'],
			summary:
				'Machine Label Generator reads equipment assignments from county workbooks and creates organized, printable PDF labels for election machines, polling locations, and spare equipment.',
			problem: [
				'Preparing equipment labels manually required staff to copy county names, polling-place names, and machine types from spreadsheets into a separate label layout.',
				'Large equipment deployments can require many labels, including duplicate machine types at the same location and special labels for spare units. Manual creation made numbering and formatting difficult to keep consistent.',
				'The generator automates the conversion from spreadsheet data to print-ready labels so that the information is produced directly from the operational source files.'
			],
			workflow: [
				'The application opens each county workbook and reads the rows containing polling locations and assigned equipment quantities.',
				'For every required machine, it creates a label containing the county, polling location, and equipment type.',
				'When multiple machines of the same type are assigned to one location, the program creates separate labels and applies sequential numbering where appropriate.',
				'Spare equipment is handled independently so that spare labels remain clearly identifiable and are not confused with polling-location assignments.',
				'The labels are arranged in a fixed grid with consistent dimensions, borders, spacing, and centered text before being written to county-specific PDF files.'
			],
			implementation: [
				'Apache POI supplies the spreadsheet-reading layer, allowing the application to use the same source workbooks already maintained by staff.',
				'Java business logic converts spreadsheet quantities into individual label records and determines when numbering or duplicate output is required.',
				'The PDF generation layer calculates label positions on each page, starts new pages when the grid is full, and preserves a uniform printable layout.',
				'Output is organized by county, which makes the generated files easier to distribute, review, reprint, and archive.'
			],
			features: [
				'Reads equipment information directly from county workbooks',
				'Creates labels for Scan, ADA, and Print equipment',
				'Includes county, polling location, and machine type',
				'Numbers repeated equipment assignments',
				'Handles spare machines separately',
				'Produces a consistent print-ready PDF layout'
			],
			input: 'County machine-assignment and polling-location Excel workbooks.',
			output: 'County-specific PDF documents containing printable equipment labels.',
			impact:
				'The tool removes a large amount of repetitive document preparation, improves label accuracy, and ensures that every county receives labels with the same structure and visual format. Updated workbooks can be processed again without rebuilding the labels by hand.'
		},
		{
			number: '03',
			title: 'Setting Scheduler',
			github: 'https://github.com/bgabr001/SettingScheduler',
			technologies: ['Java', 'Gradle', 'Apache POI', 'iCalendar'],
			summary:
				'Setting Scheduler converts a shared Excel work schedule into individual iCalendar files that employees can import into Apple Calendar, Microsoft Outlook, Google Calendar, and other compatible applications.',
			problem: [
				'Employee assignments were maintained in a shared spreadsheet, but each employee still had to review the schedule and manually add the relevant dates, times, counties, and locations to a personal calendar.',
				'Manual calendar entry created opportunities for missed assignments, incorrect times, incomplete addresses, and inconsistent event descriptions.',
				'The scheduler bridges the spreadsheet and calendar workflows by transforming approved schedule data into ready-to-import calendar events for each assigned employee.'
			],
			workflow: [
				'The application reads the main schedule workbook and identifies each date, county assignment, employee name, and optional time range.',
				'It reads a supporting address workbook and matches each county with its location and available administrative details.',
				'Custom time values are interpreted when they are present; otherwise, the application applies configured default start and end times.',
				'Assignments are grouped by employee so that every person receives only the events associated with that person.',
				'The program writes a separate .ics file for each employee, including event titles, dates, times, locations, descriptions, and stable identifiers for calendar re-importing.'
			],
			implementation: [
				'Apache POI reads both the scheduling workbook and the supporting address data, allowing the system to work with the organization’s existing Excel process.',
				'Java date-and-time logic validates schedule values, converts human-entered time formats, and applies defaults when information is incomplete.',
				'The iCalendar output follows the standard VEVENT structure so the files can be imported by common desktop, mobile, and web calendar applications.',
				'Stable event identifiers help calendar applications recognize previously imported assignments and reduce duplicate-event problems when an updated schedule is imported.'
			],
			features: [
				'Reads employee assignments from an Excel schedule',
				'Recognizes dates, counties, and custom appointment times',
				'Uses default start and end times when none are supplied',
				'Connects assignments with county addresses and administrator details',
				'Creates a separate iCalendar file for each employee',
				'Uses stable event identifiers to support calendar updates'
			],
			input: 'An employee schedule workbook and a county-address workbook.',
			output: 'Individual .ics calendar files for each scheduled employee.',
			impact:
				'The scheduler reduces calendar-entry work, provides employees with consistent event information, and makes changes easier to distribute. It also demonstrates integration between spreadsheet data and an industry-standard calendar format.'
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
				<h2>Turning operational spreadsheets into usable business systems.</h2>
			</div>
			<div class="overview-copy">
				<p>
					This collection contains three Java automation tools developed to solve real
					operational problems. Each application takes an existing manual process and
					converts it into a repeatable software workflow.
				</p>
				<p>
					Together, the applications process Excel workbooks, calculate equipment
					requirements, generate printable PDF labels, and convert employee schedules into
					calendar events.
				</p>
			</div>
		</div>

		<div class="summary-grid">
			<div class="summary-card"><strong>3</strong><span>Automation applications</span></div>
			<div class="summary-card"><strong>Java</strong><span>Primary language</span></div>
			<div class="summary-card"><strong>Excel</strong><span>Primary data source</span></div>
			<div class="summary-card"><strong>PDF + ICS</strong><span>Generated documents</span></div>
		</div>
	</div>
</section>

{#each tools as tool (tool.number)}
	<section class="section tool-section">
		<div class="page-shell">
			<article class="tool-detail">
				<div class="tool-heading">
					<span class="project-number">{tool.number}</span>

					<div>
						<div class="project-meta">
							{#each tool.technologies as technology (technology)}
								<span>{technology}</span>
							{/each}
						</div>

						<h2>{tool.title}</h2>
						<p class="tool-description">{tool.summary}</p>

						<div class="project-links">
							<a
								href={tool.github}
								target="_blank"
								rel="external noreferrer"
								class="github-link"
								aria-label={`View the ${tool.title} source code on GitHub`}
							>
								View Source Code on GitHub
								<span aria-hidden="true">→</span>
							</a>
						</div>
					</div>
				</div>

				<div class="detail-grid">
					<section class="detail-panel">
						<p class="panel-label">Purpose and Business Problem</p>

						{#each tool.problem as paragraph (paragraph)}
							<p>{paragraph}</p>
						{/each}
					</section>

					<section class="detail-panel">
						<p class="panel-label">How the Application Works</p>

						<ol class="process-list">
							{#each tool.workflow as step (step)}
								<li>{step}</li>
							{/each}
						</ol>
					</section>

					<section class="detail-panel full-width">
						<p class="panel-label">Technical Implementation</p>

						<div class="implementation-grid">
							{#each tool.implementation as item (item)}
								<p>{item}</p>
							{/each}
						</div>
					</section>
				</div>

				<div class="tool-lower-grid">
					<div>
						<h3>Key Features</h3>

						<ul class="feature-list">
							{#each tool.features as feature (feature)}
								<li>{feature}</li>
							{/each}
						</ul>
					</div>

					<div>
						<h3>Business Impact</h3>
						<p class="impact-copy">{tool.impact}</p>
					</div>
				</div>

				<div class="workflow-grid">
					<div class="workflow-card">
						<span>Input</span>
						<p>{tool.input}</p>
					</div>

					<div class="workflow-arrow" aria-hidden="true">→</div>

					<div class="workflow-card">
						<span>Output</span>
						<p>{tool.output}</p>
					</div>
				</div>
			</article>
		</div>
	</section>
{/each}

<section class="section results-section">
	<div class="page-shell">
		<div class="project-overview">
			<div>
				<p class="section-label">Business Value</p>
				<h2>Designed around measurable workflow improvements.</h2>
			</div>
			<div class="overview-copy">
				<p>
					These applications reduce the time required to review files, perform calculations,
					prepare documents, and enter schedule information manually.
				</p>
				<p>
					They also provide consistent outputs, centralized information, and reusable
					processes that can be run whenever the source information changes.
				</p>
			</div>
		</div>

		<div class="value-grid">
			<div class="value-card">
				<h3>Reduced Manual Entry</h3>
				<p>Information is extracted directly from existing spreadsheets instead of being retyped into separate documents.</p>
			</div>
			<div class="value-card">
				<h3>Consistent Output</h3>
				<p>Generated workbooks, labels, and calendar files follow standardized formats.</p>
			</div>
			<div class="value-card">
				<h3>Reusable Workflows</h3>
				<p>The applications can process updated source files without rebuilding the output manually.</p>
			</div>
		</div>
	</div>
</section>

<style>
	.back-link {
		display: inline-block;
		margin-bottom: 1.5rem;
		color: inherit;
		font-weight: 700;
		text-decoration: none;
		transition:
			transform 0.2s ease,
			opacity 0.2s ease;
	}

	.back-link:hover {
		transform: translateX(-4px);
		opacity: 0.75;
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
		line-height: 1.08;
	}

	.section-label,
	.panel-label {
		margin: 0 0 0.85rem;
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

	.summary-card,
	.workflow-card,
	.value-card,
	.detail-panel {
		border: 1px solid rgba(127, 127, 127, 0.25);
		border-radius: 18px;
		background: rgba(127, 127, 127, 0.06);
	}

	.summary-card {
		display: flex;
		flex-direction: column;
		gap: 0.4rem;
		padding: 1.5rem;
	}

	.summary-card strong {
		font-size: 1.6rem;
	}

	.summary-card span {
		opacity: 0.72;
	}

	.tool-section,
	.results-section {
		border-top: 1px solid rgba(127, 127, 127, 0.25);
	}

	.tool-detail {
		width: min(100%, 1180px);
		margin: 0 auto;
	}

	.tool-heading {
		display: grid;
		grid-template-columns: 72px minmax(0, 1fr);
		gap: 2rem;
		align-items: start;
	}

	.project-number {
		display: inline-flex;
		align-items: center;
		justify-content: center;
		width: 58px;
		height: 58px;
		margin-top: 0.15rem;
		border: 1px solid rgba(127, 127, 127, 0.35);
		border-radius: 50%;
		font-size: 0.95rem;
		font-weight: 800;
	}

	.project-meta {
		display: flex;
		flex-wrap: wrap;
		gap: 0.65rem;
	}

	.project-meta span {
		padding: 0.45rem 0.85rem;
		border: 1px solid rgba(127, 127, 127, 0.25);
		border-radius: 999px;
		background: rgba(127, 127, 127, 0.05);
		font-size: 0.76rem;
		font-weight: 700;
		letter-spacing: 0.04em;
	}

	.tool-heading h2 {
		margin: 1rem 0 1rem;
		font-size: clamp(2.4rem, 5vw, 4.25rem);
		line-height: 1.02;
		letter-spacing: -0.035em;
	}

	.tool-description {
		max-width: 920px;
		margin: 0;
		font-size: 1.08rem;
		line-height: 1.8;
	}


	.project-links {
		display: flex;
		flex-wrap: wrap;
		gap: 0.9rem;
		margin-top: 1.5rem;
	}

	.github-link {
		display: inline-flex;
		align-items: center;
		gap: 0.55rem;
		width: fit-content;
		padding: 0.8rem 1.1rem;
		border: 1px solid rgba(127, 127, 127, 0.3);
		border-radius: 999px;
		color: inherit;
		background: rgba(127, 127, 127, 0.07);
		font-size: 0.9rem;
		font-weight: 800;
		text-decoration: none;
		transition:
			transform 0.2s ease,
			border-color 0.2s ease,
			background 0.2s ease;
	}

	.github-link:hover {
		transform: translateY(-2px);
		border-color: rgba(127, 127, 127, 0.55);
		background: rgba(127, 127, 127, 0.12);
	}

	.github-link:focus-visible {
		outline: 3px solid currentColor;
		outline-offset: 4px;
	}

	.detail-grid {
		display: grid;
		grid-template-columns: repeat(2, minmax(0, 1fr));
		gap: 1.25rem;
		margin-top: 3rem;
	}

	.detail-panel {
		padding: clamp(1.5rem, 3vw, 2.25rem);
	}

	.detail-panel.full-width {
		grid-column: 1 / -1;
	}

	.panel-label {
		padding-bottom: 0.9rem;
		border-bottom: 1px solid rgba(127, 127, 127, 0.2);
	}

	.detail-panel p {
		margin: 0;
		font-size: 1rem;
		line-height: 1.78;
	}

	.detail-panel p + p {
		margin-top: 1.15rem;
	}

	.process-list {
		display: grid;
		gap: 1rem;
		margin: 0;
		padding-left: 1.45rem;
		line-height: 1.7;
	}

	.process-list li {
		padding-left: 0.4rem;
	}

	.process-list li::marker {
		font-weight: 800;
	}

	.implementation-grid {
		display: grid;
		grid-template-columns: repeat(2, minmax(0, 1fr));
		gap: 1.25rem;
	}

	.implementation-grid p {
		padding: 1.15rem;
		border: 1px solid rgba(127, 127, 127, 0.18);
		border-radius: 14px;
		background: rgba(127, 127, 127, 0.035);
	}

	.tool-lower-grid {
		display: grid;
		grid-template-columns: repeat(2, minmax(0, 1fr));
		gap: 1.25rem;
		margin-top: 1.25rem;
	}

	.tool-lower-grid > div {
		padding: clamp(1.5rem, 3vw, 2.25rem);
		border: 1px solid rgba(127, 127, 127, 0.25);
		border-radius: 18px;
		background: rgba(127, 127, 127, 0.06);
	}

	.tool-lower-grid h3 {
		margin: 0;
		padding-bottom: 0.9rem;
		border-bottom: 1px solid rgba(127, 127, 127, 0.2);
		font-size: 1rem;
		font-weight: 800;
		letter-spacing: 0.12em;
		text-transform: uppercase;
	}

	.feature-list {
		display: grid;
		gap: 0.8rem;
		margin: 1.25rem 0 0;
		padding-left: 1.3rem;
		line-height: 1.65;
	}

	.impact-copy {
		margin: 1.25rem 0 0;
		line-height: 1.8;
	}

	.workflow-grid {
		display: grid;
		grid-template-columns: minmax(0, 1fr) 56px minmax(0, 1fr);
		gap: 1rem;
		margin-top: 1.25rem;
		align-items: stretch;
	}

	.workflow-card {
		display: flex;
		min-height: 150px;
		padding: 1.5rem;
		flex-direction: column;
		justify-content: center;
	}

	.workflow-card span {
		display: block;
		margin-bottom: 0.7rem;
		font-size: 0.75rem;
		font-weight: 800;
		letter-spacing: 0.14em;
		text-transform: uppercase;
		opacity: 0.72;
	}

	.workflow-card p {
		margin: 0;
		line-height: 1.65;
	}

	.workflow-arrow {
		display: grid;
		place-items: center;
		font-size: 1.75rem;
		font-weight: 800;
		opacity: 0.65;
	}

	.value-grid {
		display: grid;
		grid-template-columns: repeat(3, minmax(0, 1fr));
		gap: 1rem;
		margin-top: 3rem;
	}

	.value-card {
		padding: 1.5rem;
	}

	.value-card h3 {
		margin: 0 0 0.75rem;
	}

	.value-card p {
		margin: 0;
		line-height: 1.7;
	}

	@media (max-width: 900px) {
		.project-overview,
		.detail-grid,
		.tool-lower-grid,
		.implementation-grid {
			grid-template-columns: 1fr;
			gap: 1.25rem;
		}

		.detail-panel.full-width {
			grid-column: auto;
		}

		.summary-grid {
			grid-template-columns: repeat(2, minmax(0, 1fr));
		}

		.value-grid {
			grid-template-columns: 1fr;
		}

		.tool-heading {
			grid-template-columns: 60px minmax(0, 1fr);
			gap: 1.25rem;
		}
	}

	@media (max-width: 600px) {
		.summary-grid,
		.workflow-grid {
			grid-template-columns: 1fr;
		}

		.workflow-arrow {
			min-height: 40px;
			transform: rotate(90deg);
		}

		.tool-heading {
			grid-template-columns: 1fr;
		}

		.project-number {
			width: 48px;
			height: 48px;
		}

		.tool-heading h2 {
			font-size: clamp(2.2rem, 12vw, 3.25rem);
		}
	}
</style>
