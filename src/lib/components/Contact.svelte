<section id="contact" class="contact">
	<div class="container">
		<header class="sec-head">
			<span class="num">03</span>
			<h2>Contact</h2>
		</header>

		<p class="lead">
			기획·디자인·개발 사이를 좁히는 일에 관심 있다면 환영합니다.<br />
			협업 제안도, 가벼운 대화도 모두 좋아요.
		</p>

		<a class="email" href="mailto:6464106@gmail.com">
			6464106@gmail.com
			<span class="arrow" aria-hidden="true">↗</span>
		</a>

		<div class="links">
			<a href="https://github.com/Yeonho-Lee" target="_blank" rel="noopener noreferrer">
				<span class="link-label">GITHUB</span>
				<span class="link-val">github.com/Yeonho-Lee</span>
			</a>
			<a href="tel:01065706114">
				<span class="link-label">PHONE</span>
				<span class="link-val">010-6570-6114</span>
			</a>
			<div class="link-static">
				<span class="link-label">LOCATION</span>
				<span class="link-val">서울시 관악구</span>
			</div>
		</div>

		<footer class="foot">
			<span>© 2026 Yeonho Lee</span>
			<span>Built with SvelteKit</span>
		</footer>
	</div>
</section>

<style>
	.contact {
		padding: 140px 0 60px;
		border-top: 1px solid var(--line);
	}

	.container {
		max-width: 1100px;
		margin: 0 auto;
		padding: 0 32px;
	}

	.sec-head {
		display: flex;
		align-items: baseline;
		gap: 16px;
		margin-bottom: 64px;
	}

	.num {
		font-family: 'Barlow', sans-serif;
		font-size: 13px;
		font-weight: 600;
		color: var(--accent);
		letter-spacing: 0.1em;
	}

	h2 {
		font-family: 'Barlow', sans-serif;
		font-size: clamp(32px, 5vw, 56px);
		font-weight: 700;
		letter-spacing: -0.02em;
	}

	.lead {
		font-size: clamp(20px, 3vw, 32px);
		font-weight: 300;
		color: var(--mid);
		line-height: 1.5;
		margin-bottom: 48px;
		word-break: keep-all;
	}

	.email {
		display: inline-flex;
		align-items: center;
		gap: 12px;
		font-family: 'Barlow', sans-serif;
		font-size: clamp(28px, 5vw, 56px);
		font-weight: 700;
		color: var(--ink);
		padding-bottom: 8px;
		border-bottom: 2px solid var(--line);
		transition:
			color 0.2s,
			border-color 0.2s;
		margin-bottom: 80px;
	}

	.email:hover {
		color: var(--accent);
		border-bottom-color: var(--accent);
	}

	.email .arrow {
		font-size: 0.7em;
		transition: transform 0.2s;
	}

	.email:hover .arrow {
		transform: translate(4px, -4px);
	}

	.links {
		display: grid;
		grid-template-columns: repeat(3, 1fr);
		gap: 32px;
		padding-top: 32px;
		border-top: 1px solid var(--line);
	}

	.links a,
	.link-static {
		display: flex;
		flex-direction: column;
		gap: 6px;
		transition: color 0.2s;
	}

	.links a:hover {
		color: var(--accent);
	}

	.link-label {
		font-family: 'Barlow', sans-serif;
		font-size: 11px;
		font-weight: 600;
		letter-spacing: 0.2em;
		color: var(--muted);
	}

	.link-val {
		font-size: 14px;
		color: var(--ink);
	}

	.foot {
		display: flex;
		justify-content: space-between;
		align-items: center;
		margin-top: 96px;
		padding-top: 24px;
		border-top: 1px solid var(--line);
		font-family: 'Barlow', sans-serif;
		font-size: 11px;
		color: var(--muted);
		letter-spacing: 0.1em;
	}

	@media (max-width: 768px) {
		.contact {
			padding: 96px 0 48px;
		}
		.links {
			grid-template-columns: 1fr;
			gap: 20px;
		}
		.foot {
			flex-direction: column;
			gap: 8px;
			align-items: flex-start;
		}
	}
</style>
