<script lang="ts">
	import '../app.css';
	import { base } from '$app/paths';
	import { page } from '$app/stores';

	const links = [
		{ label: 'Home', href: `${base}/` },
		{ label: 'About', href: `${base}/about` },
		{ label: 'Projects', href: `${base}/projects` },
		{ label: 'Experience', href: `${base}/experience` },
		{ label: 'Resume', href: `${base}/resume` },
		{ label: 'Contact', href: `${base}/contact` }
	];

	let menuOpen = false;

	function isActive(href: string, pathname: string) {
		if (href === `${base}/`) return pathname === `${base}/`;
		return pathname.startsWith(href);
	}
</script>

<svelte:head>
	<meta
		name="description"
		content="The software development portfolio of Brennen Gabriel."
	/>
</svelte:head>

<header class="site-header">
	<div class="nav-shell">
		<a class="brand" href={`${base}/`} aria-label="Brennen Gabriel home">
			<span class="brand-mark">BG</span>
			<span class="brand-name">Brennen Gabriel</span>
		</a>

		<button
			class="menu-button"
			type="button"
			aria-label="Toggle navigation"
			aria-expanded={menuOpen}
			on:click={() => (menuOpen = !menuOpen)}
		>
			<span></span>
			<span></span>
			<span></span>
		</button>

		<nav class:open={menuOpen} aria-label="Main navigation">
			{#each links as link}
				<a
					href={link.href}
					class:active={isActive(link.href, $page.url.pathname)}
					on:click={() => (menuOpen = false)}
				>
					{link.label}
				</a>
			{/each}
		</nav>
	</div>
</header>

<main>
	<slot />
</main>

<footer class="site-footer">
	<div class="footer-shell">
		<p>© {new Date().getFullYear()} Brennen Gabriel</p>
		<p>Built with SvelteKit</p>
	</div>
</footer>
