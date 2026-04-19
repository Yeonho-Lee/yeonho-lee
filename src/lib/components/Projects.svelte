<script lang="ts">
	type Item = {
		org: string;
		role: string;
		period: string;
		desc: string[];
		tag: 'work' | 'project';
	};

	const items: Item[] = [
		{
			tag: 'work',
			org: '교육청 학습 지원 포털',
			role: '프론트엔드 개발자 · 프리랜서',
			period: '2026.01 — 현재',
			desc: [
				'경계선지능·난독증 학생 교육 지원 관리 시스템 프론트엔드 개발',
				'학생 신청·치료사 배정·교육청·관리자 등 역할별 인터페이스 전체 구현',
				'SvelteKit(Svelte 5) + TypeScript + Drizzle ORM + Tailwind CSS v4',
				'JWT 인증·개인정보 암호화 적용'
			]
		},
		{
			tag: 'work',
			org: '교육청 분수 학습 프로그램',
			role: '프론트엔드 개발자 · 계약직',
			period: '2025.09 — 2025.12',
			desc: [
				'Svelte + TypeScript로 분수 개념 시각화 애니메이션 컴포넌트 제작',
				'콘텐츠와 재생 로직 분리 구조로 설계해 한 차시 제작 시간 대폭 단축'
			]
		},
		{
			tag: 'project',
			org: '당신은 한국 사회에 대해 얼마나 잘 알고 계신가요?',
			role: '프론트엔드 개발 · p5.js, React',
			period: '2024.03 — 2024.06',
			desc: [
				'사회 문제 통계를 100인 시각화로 표현하는 데이터 시각화 웹 프로젝트',
				'p5.js로 유저 답변에 반응하는 100인 애니메이션 구현, 초기화 코드 분리로 렌더링 버그 해결',
				'React 기반 페이지 구성, 디자인·기획·개발 동시 진행 조율'
			]
		},
		{
			tag: 'project',
			org: 'EmoStock',
			role: 'UX 디자인 · Figma, Python',
			period: '2023.09 — 2023.12',
			desc: [
				'감정 일지 + 주식 거래 기록·분석 앱',
				'Figma로 전체 UI/UX 설계, Python으로 주식 데이터 크롤링',
				'5회 이터레이션 애자일, 매 이터레이션 전 화면 흐름 공유로 디자인-개발 충돌 해소'
			]
		},
		{
			tag: 'project',
			org: '모바일 인게임 광고 UX 개선방안',
			role: 'UX 리서치',
			period: '2023.03 — 2023.06',
			desc: [
				'모바일 게임 팝업 광고의 불쾌감 문제를 HCI 관점에서 연구',
				'게임 이용자·개발자 인터뷰를 통해 원인 분석, 사용자 중심 개선안 도출'
			]
		},
		{
			tag: 'project',
			org: 'Everywear',
			role: '기획 · 앱 프로토타입',
			period: '2022.09 — 2022.12',
			desc: ['지역 세탁소 인프라를 활용한 저가 중고 의류 접근 앱 기획 및 프로토타입 제작']
		},
		{
			tag: 'project',
			org: 'Lovster Hotel',
			role: '개발 · Processing',
			period: '2019.03 — 2019.06',
			desc: ['영화 "The Lobster"에서 영감을 받아 Processing으로 제작한 시뮬레이션 게임']
		}
	];
</script>

<section id="projects" class="projects">
	<div class="container">
		<header class="sec-head">
			<span class="num">02</span>
			<h2>Work &amp; Projects</h2>
		</header>

		<div class="list">
			{#each items as item, i (item.org + i)}
				<article class="item">
					<div class="item-meta">
						<span class="tag">{item.tag === 'work' ? 'WORK' : 'PROJECT'}</span>
						<span class="period">{item.period}</span>
					</div>
					<div class="item-body">
						<h3>{item.org}</h3>
						<p class="role">{item.role}</p>
						<ul>
							<!-- eslint-disable-next-line svelte/require-each-key -->
							{#each item.desc as line}
								<li>{line}</li>
							{/each}
						</ul>
					</div>
				</article>
			{/each}
		</div>
	</div>
</section>

<style>
	.projects {
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

	.list {
		display: flex;
		flex-direction: column;
	}

	.item {
		display: grid;
		grid-template-columns: 200px 1fr;
		gap: 48px;
		padding: 32px 0;
		border-top: 1px solid var(--line);
		transition: padding 0.3s ease;
	}

	.item:last-child {
		border-bottom: 1px solid var(--line);
	}

	.item:hover {
		padding-left: 12px;
	}

	.item-meta {
		display: flex;
		flex-direction: column;
		gap: 8px;
	}

	.tag {
		font-family: 'Barlow', sans-serif;
		font-size: 10px;
		font-weight: 700;
		letter-spacing: 0.2em;
		color: var(--accent);
		background: var(--accent-soft);
		padding: 4px 10px;
		border-radius: 4px;
		width: fit-content;
	}

	.period {
		font-family: 'Barlow', sans-serif;
		font-size: 12px;
		color: var(--muted);
		letter-spacing: 0.05em;
	}

	.item h3 {
		font-family: 'Barlow', sans-serif;
		font-size: 22px;
		font-weight: 700;
		color: var(--ink);
		margin-bottom: 6px;
		word-break: keep-all;
	}

	.role {
		font-size: 13px;
		color: var(--mid);
		margin-bottom: 16px;
	}

	ul {
		list-style: none;
	}

	li {
		font-size: 14px;
		color: var(--mid);
		line-height: 1.75;
		padding-left: 16px;
		position: relative;
		word-break: keep-all;
		margin-bottom: 4px;
	}

	li::before {
		content: '';
		position: absolute;
		left: 0;
		top: 12px;
		width: 6px;
		height: 1px;
		background: var(--muted);
	}

	@media (max-width: 768px) {
		.projects {
			padding: 96px 0;
		}
		.item {
			grid-template-columns: 1fr;
			gap: 16px;
			padding: 24px 0;
		}
		.item:hover {
			padding-left: 0;
		}
		.item-meta {
			flex-direction: row;
			align-items: center;
			gap: 12px;
		}
	}
</style>
