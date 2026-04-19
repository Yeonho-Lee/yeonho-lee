<section id="about" class="about">
	<div class="container">
		<header class="sec-head">
			<span class="num">01</span>
			<h2>About</h2>
		</header>

		<div class="grid">
			<div class="col-left">
				<p class="lead">
					학부 시절 기획과 디자인을 하며 사용자 경험을 설계했지만, 프로토타입을 넘기고 나면 의도한
					흐름이 그대로 구현되지 않는 일이 반복됐습니다. 직접 만들 수 없는 한계를 느끼고 개발에
					뛰어들었습니다.
				</p>
				<p class="body">
					현재 SvelteKit과 TypeScript로 교육청 학습 지원 포털을 실무 개발하며, JWT 인증·개인정보
					암호화 등 보안 요소까지 직접 구현하고 있습니다.
				</p>
			</div>

			<div class="col-right">
				<div class="card">
					<h3>Strengths</h3>
					<ul>
						<li>구조를 먼저 생각하는 설계 습관</li>
						<li>기획·디자인 경험이 뒷받침하는 구현</li>
						<li>역할별 사용자 흐름을 그리는 사고</li>
					</ul>
				</div>
				<div class="card">
					<h3>Currently Learning</h3>
					<ul>
						<li>Java 기초 — 백엔드 구조 이해</li>
						<li>Svelte 5 Runes 심화</li>
						<li>접근성·웹 성능 최적화</li>
					</ul>
				</div>
			</div>
		</div>

		<div class="skills">
			<h3 class="skills-title">Skills</h3>
			<div class="skill-grid">
				<div class="skill-row">
					<span class="cat">Languages</span>
					<span class="val">JavaScript · TypeScript · HTML / CSS · Java · Python</span>
				</div>
				<div class="skill-row">
					<span class="cat">Framework</span>
					<span class="val">Svelte · SvelteKit</span>
				</div>
				<div class="skill-row">
					<span class="cat">Database</span>
					<span class="val">Drizzle ORM</span>
				</div>
				<div class="skill-row">
					<span class="cat">Tools</span>
					<span class="val">Git · Figma · p5.js · Processing · pnpm</span>
				</div>
			</div>
		</div>

		<div class="edu">
			<h3 class="skills-title">Education</h3>
			<div class="edu-row">
				<div>
					<div class="edu-name">서울대학교</div>
					<div class="edu-detail">자유전공학부 · 학사</div>
				</div>
				<span class="edu-period">2015.03 — 2026.08</span>
			</div>
			<div class="edu-row">
				<div>
					<div class="edu-name">강원과학고등학교</div>
				</div>
				<span class="edu-period">2013.03 — 2015.02</span>
			</div>
		</div>
	</div>
</section>

<style>
	.about {
		padding: 140px 0;
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

	.grid {
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: 64px;
		margin-bottom: 96px;
	}

	.lead {
		font-size: 18px;
		line-height: 1.8;
		color: var(--ink);
		margin-bottom: 24px;
		word-break: keep-all;
	}

	.body {
		font-size: 15px;
		color: var(--mid);
		word-break: keep-all;
	}

	.col-right {
		display: flex;
		flex-direction: column;
		gap: 20px;
	}

	.card {
		background: var(--bg-card);
		border: 1px solid var(--line);
		border-radius: 8px;
		padding: 24px;
	}

	.card h3 {
		font-family: 'Barlow', sans-serif;
		font-size: 11px;
		font-weight: 700;
		letter-spacing: 0.2em;
		text-transform: uppercase;
		color: var(--accent);
		margin-bottom: 16px;
	}

	.card ul {
		list-style: none;
	}

	.card li {
		font-size: 14px;
		color: var(--mid);
		padding: 6px 0;
		border-bottom: 1px solid var(--line);
	}

	.card li:last-child {
		border-bottom: none;
	}

	.skills,
	.edu {
		margin-top: 64px;
	}

	.skills-title {
		font-family: 'Barlow', sans-serif;
		font-size: 11px;
		font-weight: 700;
		letter-spacing: 0.2em;
		text-transform: uppercase;
		color: var(--muted);
		margin-bottom: 24px;
	}

	.skill-grid {
		border-top: 1px solid var(--line);
	}

	.skill-row {
		display: grid;
		grid-template-columns: 160px 1fr;
		gap: 32px;
		padding: 18px 0;
		border-bottom: 1px solid var(--line);
		align-items: baseline;
	}

	.cat {
		font-family: 'Barlow', sans-serif;
		font-size: 12px;
		font-weight: 600;
		letter-spacing: 0.15em;
		text-transform: uppercase;
		color: var(--muted);
	}

	.val {
		font-size: 15px;
		color: var(--ink);
	}

	.edu-row {
		display: flex;
		justify-content: space-between;
		align-items: baseline;
		padding: 18px 0;
		border-bottom: 1px solid var(--line);
	}

	.edu-row:first-of-type {
		border-top: 1px solid var(--line);
	}

	.edu-name {
		font-family: 'Barlow', sans-serif;
		font-size: 16px;
		font-weight: 700;
		color: var(--ink);
	}

	.edu-detail {
		font-size: 13px;
		color: var(--mid);
		margin-top: 4px;
	}

	.edu-period {
		font-family: 'Barlow', sans-serif;
		font-size: 12px;
		color: var(--muted);
		letter-spacing: 0.05em;
	}

	@media (max-width: 768px) {
		.about {
			padding: 96px 0;
		}
		.grid {
			grid-template-columns: 1fr;
			gap: 48px;
			margin-bottom: 64px;
		}
		.skill-row {
			grid-template-columns: 1fr;
			gap: 6px;
		}
	}
</style>
