<script lang="ts">
	import favicon from '$lib/assets/favicon.svg';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
	<link rel="preconnect" href="https://fonts.googleapis.com" />
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin="anonymous" />
	<link
		href="https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@300;400;500;700&family=Barlow:wght@400;600;700&display=swap"
		rel="stylesheet"
	/>
</svelte:head>

{@render children()}

<style>
	:global(:root) {
		--bg: #0a0a0c;
		--bg-elev: #131318;
		--bg-card: #17171d;
		--ink: #f2f2f3;
		--mid: #a8a8b3;
		--muted: #6b6b78;
		--line: #25252e;
		--accent: #6ea8ff;
		--accent-soft: rgba(110, 168, 255, 0.12);
	}

	:global(*) {
		margin: 0;
		padding: 0;
		box-sizing: border-box;
	}

	:global(html) {
		scroll-behavior: smooth;
	}

	:global(body) {
		background: var(--bg);
		color: var(--ink);
		font-family: 'Noto Sans KR', sans-serif;
		font-size: 15px;
		line-height: 1.7;
		-webkit-font-smoothing: antialiased;
		-moz-osx-font-smoothing: grayscale;
	}

	:global(a) {
		color: inherit;
		text-decoration: none;
	}

	:global(::selection) {
		background: var(--accent-soft);
		color: var(--ink);
	}
</style>
