<section id="hero" class="hero">
	<div class="container">
		<p class="eyebrow">Frontend Developer</p>
		<h1 class="name">
			Yeonho<br />
			<span class="name-accent">Lee</span>
		</h1>
		<p class="tagline">
			사용자 흐름을 코드로 직접 연결하는 개발자.<br />
			기획·디자인·개발의 간격을 좁히는 UX 엔지니어를 지향합니다.
		</p>
		<div class="meta">
			<span>이연호</span>
			<span class="dot"></span>
			<span>Seoul, KR</span>
			<span class="dot"></span>
			<span>1997.03.26</span>
		</div>
	</div>
	<div class="scroll-hint" aria-hidden="true">
		<span>SCROLL</span>
		<div class="line"></div>
	</div>
</section>

<style>
	.hero {
		min-height: 100vh;
		display: flex;
		flex-direction: column;
		justify-content: center;
		position: relative;
		padding: 120px 0 80px;
	}

	.container {
		max-width: 1100px;
		margin: 0 auto;
		padding: 0 32px;
		width: 100%;
	}

	.eyebrow {
		font-family: 'Barlow', sans-serif;
		font-size: 13px;
		font-weight: 600;
		letter-spacing: 0.25em;
		text-transform: uppercase;
		color: var(--accent);
		margin-bottom: 24px;
	}

	.name {
		font-family: 'Barlow', sans-serif;
		font-size: clamp(64px, 12vw, 144px);
		font-weight: 700;
		line-height: 0.95;
		letter-spacing: -0.02em;
		margin-bottom: 32px;
	}

	.name-accent {
		color: var(--mid);
	}

	.tagline {
		font-size: clamp(15px, 1.4vw, 18px);
		color: var(--mid);
		max-width: 560px;
		line-height: 1.8;
		margin-bottom: 40px;
		word-break: keep-all;
	}

	.meta {
		display: flex;
		align-items: center;
		gap: 14px;
		font-family: 'Barlow', sans-serif;
		font-size: 13px;
		color: var(--muted);
		letter-spacing: 0.05em;
	}

	.dot {
		width: 3px;
		height: 3px;
		border-radius: 50%;
		background: var(--muted);
	}

	.scroll-hint {
		position: absolute;
		bottom: 40px;
		left: 50%;
		transform: translateX(-50%);
		display: flex;
		flex-direction: column;
		align-items: center;
		gap: 12px;
		font-family: 'Barlow', sans-serif;
		font-size: 10px;
		letter-spacing: 0.3em;
		color: var(--muted);
	}

	.line {
		width: 1px;
		height: 40px;
		background: linear-gradient(to bottom, var(--muted), transparent);
		animation: scroll-line 2s ease-in-out infinite;
	}

	@keyframes scroll-line {
		0%,
		100% {
			transform: scaleY(0.5);
			transform-origin: top;
		}
		50% {
			transform: scaleY(1);
			transform-origin: top;
		}
	}

	@media (max-width: 640px) {
		.scroll-hint {
			display: none;
		}
	}
</style>
