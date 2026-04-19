<script lang="ts">
	import Hero from '$lib/components/Hero.svelte';
	import About from '$lib/components/About.svelte';
	import Projects from '$lib/components/Projects.svelte';
	import Contact from '$lib/components/Contact.svelte';

	const navItems = [
		{ id: 'hero', label: 'Home' },
		{ id: 'about', label: 'About' },
		{ id: 'projects', label: 'Work' },
		{ id: 'contact', label: 'Contact' }
	];

	let active = $state('hero');
	let scrolled = $state(false);

	function onScroll() {
		scrolled = window.scrollY > 20;
		const offset = window.innerHeight / 3;
		for (const item of navItems) {
			const el = document.getElementById(item.id);
			if (!el) continue;
			const top = el.getBoundingClientRect().top;
			if (top <= offset) active = item.id;
		}
	}
</script>

<svelte:head>
	<title>Yeonho Lee — Frontend Developer</title>
	<meta
		name="description"
		content="Frontend Developer · 사용자 흐름을 코드로 직접 연결하는 개발자."
	/>
</svelte:head>

<svelte:window on:scroll={onScroll} />

<nav class="nav" class:scrolled>
	<a class="brand" href="#hero">YL.</a>
	<ul>
		{#each navItems as item}
			<li>
				<a href="#{item.id}" class:active={active === item.id}>
					{item.label}
				</a>
			</li>
		{/each}
	</ul>
</nav>

<main>
	<Hero />
	<About />
	<Projects />
	<Contact />
</main>

<style>
	.nav {
		position: fixed;
		top: 0;
		left: 0;
		right: 0;
		z-index: 100;
		display: flex;
		align-items: center;
		justify-content: space-between;
		padding: 20px 32px;
		transition:
			background 0.3s,
			backdrop-filter 0.3s,
			border-color 0.3s,
			padding 0.3s;
		border-bottom: 1px solid transparent;
	}

	.nav.scrolled {
		background: rgba(10, 10, 12, 0.7);
		backdrop-filter: blur(12px);
		-webkit-backdrop-filter: blur(12px);
		border-bottom-color: var(--line);
		padding: 14px 32px;
	}

	.brand {
		font-family: 'Barlow', sans-serif;
		font-size: 18px;
		font-weight: 700;
		letter-spacing: -0.02em;
		color: var(--ink);
	}

	ul {
		list-style: none;
		display: flex;
		gap: 4px;
	}

	li a {
		display: block;
		padding: 8px 14px;
		font-family: 'Barlow', sans-serif;
		font-size: 12px;
		font-weight: 600;
		letter-spacing: 0.15em;
		text-transform: uppercase;
		color: var(--muted);
		border-radius: 4px;
		transition:
			color 0.2s,
			background 0.2s;
	}

	li a:hover {
		color: var(--ink);
	}

	li a.active {
		color: var(--accent);
		background: var(--accent-soft);
	}

	@media (max-width: 640px) {
		.nav {
			padding: 16px 20px;
		}
		.nav.scrolled {
			padding: 12px 20px;
		}
		li a {
			padding: 6px 10px;
			font-size: 11px;
			letter-spacing: 0.1em;
		}
	}
</style>
