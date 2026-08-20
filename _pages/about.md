---
layout: about
title: Home
permalink: /
subtitle: 

profile:
  align: right
  image: prof_pic.jpg
  image_circular: false # crops the image to make it circular
  more_info: >
    <p>Prof. Yoo Seong Choi</p>
    <p>Principal Investigator</p>
    <p>E-mail: <a href="mailto:biochoi@cnu.ac.kr">biochoi@cnu.ac.kr</a></p>

selected_papers: true # includes a list of papers marked as "selected={true}"
social: false # includes social icons at the bottom of the page

announcements:
  enabled: true # includes a list of news items
  scrollable: true # adds a vertical scroll bar if there are more than 3 news items
  limit: 5 # leave blank to include all the news in the `_news` folder

latest_posts:
  enabled: false
  scrollable: true # adds a vertical scroll bar if there are more than 3 new posts items
  limit: 3 # leave blank to include all the blog posts
---

<style>
  /* ══════════════════════════════════════════════════════════
   * 프로필 (사진 + 이름 · 직위 · 이메일)
   * ══════════════════════════════════════════════════════════ */

  /* 코드 블록 글꼴로 잡히는 것을 방지 */
  .profile .more-info {
    font-family: inherit;
    font-size: 0.95rem;
    line-height: 1.7;
  }

  .profile .more-info p {
    margin: 0;
  }

  @media (min-width: 768px) {
    .profile {
      margin-top: 5rem;
    }

    .profile .more-info {
      margin-top: 0.9rem;
      text-align: right;
    }

    /* 소개글이 사진·연락처 아래로 파고들지 않게 함 */
    .post article > .clearfix > p {
      overflow: hidden;
    }
    
    .home-brand {
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      gap: 1.5rem;
    }

    .home-brand > div {
      margin-top: 0;
    }
  }

  /* ══════════════════════════════════════════════════════════
   * 섹션 제목 — 학술지 목차의 괘선 조판
   *
   *   .home-head          → 본문에 직접 작성한 Research 제목
   *   .post article > h2  → 테마가 생성하는 News /
   *                          Selected publications 제목
   *
   * 두 선택자가 같은 선언을 공유하므로 세 제목이 동일하게 보입니다.
   * ══════════════════════════════════════════════════════════ */

  .home-head,
  .post article > h2 {
    clear: both;
    max-width: none;
    margin: 3.5rem 0 0;
    padding-bottom: 0.7rem;
    border-bottom: 2px solid var(--joinus-accent, #1a3a6b);
    color: var(--joinus-accent, #1a3a6b);
    font-size: 1.6rem;
    font-weight: 700;
    letter-spacing: -0.01em;
    line-height: 1.25;
    text-align: left;
  }

  /* 테마가 만든 제목은 소문자로 출력됩니다. */
  .post article > h2 {
    text-transform: capitalize;
  }

  .post article > h2 > a {
    text-decoration: none;
  }

  /* 국문 부제 — 영문 제목과 같은 줄에 나란히 */
  .home-head-ko,
  .post article > h2 > a::after {
    margin-left: 0.65rem;
    color: var(--global-text-color-light);
    font-size: 0.95rem;
    font-weight: 400;
    letter-spacing: 0;
    text-transform: none;
    white-space: nowrap;
  }

  .post article > h2 > a[href$="/news/"]::after {
    content: "소식";
  }

  .post article > h2 > a[href$="/publications/"]::after {
    content: "대표 논문";
  }

  /* ══════════════════════════════════════════════════════════
   * Research — 가로 띠 조판
   * ══════════════════════════════════════════════════════════ */

  .home-research {
    clear: both;
    width: 100%;
    margin: 3.5rem 0 0;
  }

  .home-research .home-head {
    margin-top: 0;
  }

  .home-areas {
    width: 100%;
    border-bottom: 1px solid var(--global-divider-color, #e0e0e0);
  }

  .home-area,
  .home-area:visited {
    display: grid;
    grid-template-columns: minmax(0, 0.85fr) minmax(0, 1.15fr);
    gap: 0.6rem 2.5rem;
    align-items: start;
    box-sizing: border-box;
    padding: 1.35rem 0;
    border-top: 1px solid var(--global-divider-color, #e0e0e0);
    color: inherit;
    text-decoration: none;
  }

  .home-area:first-child {
    padding-top: 1.6rem;
    border-top: none;
  }

  .home-area-title {
    margin: 0;
    color: var(--joinus-accent, #1a3a6b);
    font-size: 1.02rem;
    font-weight: 700;
    line-height: 1.45;
  }

  .home-area-desc {
    margin: 0;
    color: var(--global-text-color-light);
    font-size: 0.92rem;
    line-height: 1.7;
  }

  .home-area:hover,
  .home-area:focus-visible {
    color: inherit;
    text-decoration: none;
  }

  .home-area:hover .home-area-title,
  .home-area:focus-visible .home-area-title {
    text-decoration: underline;
    text-underline-offset: 4px;
  }

  .home-area:focus-visible {
    outline: 2px solid var(--global-theme-color, #1a4d3e);
    outline-offset: 2px;
  }

  .home-research-more {
    margin: 1.6rem 0 0;
    font-size: 0.92rem;
  }

  .home-research-more a {
    color: var(--global-theme-color, #1a4d3e);
    font-weight: 600;
    text-decoration: none;
  }

  .home-research-more a:hover {
    text-decoration: underline;
    text-underline-offset: 4px;
  }

  /* ══════════════════════════════════════════════════════════
   * News / Selected publications 본문 여백
   * ══════════════════════════════════════════════════════════ */

  .post article > h2 + * {
    margin-top: 1.5rem;
  }

  /* ══════════════════════════════════════════════════════════
   * Join Us — 상자가 아닌 괘선 밴드
   * ══════════════════════════════════════════════════════════ */

  .home-joinus {
    clear: both;
    display: grid;
    grid-template-columns: minmax(0, 1fr) auto;
    align-items: center;
    gap: 1.2rem 2.5rem;
    width: 100%;
    box-sizing: border-box;
    margin: 3.5rem 0 0rem;
    padding: 1.7rem 0;
    border-top: 1px solid var(--global-divider-color, #e0e0e0);
    border-bottom: 1px solid var(--global-divider-color, #e0e0e0);
  }

  .home-joinus-title {
    margin: 0 0 0.45rem;
    color: var(--joinus-accent, #1a3a6b);
    font-size: 1.08rem;
    font-weight: 700;
    line-height: 1.45;
  }

  .home-joinus-text {
    margin: 0;
    color: var(--global-text-color-light);
    font-size: 0.93rem;
    line-height: 1.6;
  }

  .home-joinus-button,
  .home-joinus-button:visited {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    min-height: 44px;
    padding: 0.75rem 1.4rem;
    border: 2px solid var(--global-theme-color, #1a4d3e);
    border-radius: 8px;
    color: var(--global-theme-color, #1a4d3e);
    font-size: 0.92rem;
    font-weight: 600;
    line-height: 1.2;
    text-decoration: none;
    white-space: nowrap;
    transition:
      background-color 0.2s ease,
      color 0.2s ease;
  }

  .home-joinus-button:hover,
  .home-joinus-button:focus-visible {
    background-color: var(--global-theme-color, #1a4d3e);
    color: var(--global-hover-text-color, #ffffff);
    text-decoration: none;
  }

  .home-joinus-button:focus-visible {
    outline: 2px solid var(--global-theme-color, #1a4d3e);
    outline-offset: 3px;
  }

  /* ══════════════════════════════════════════════════════════
   * 반응형
   * ══════════════════════════════════════════════════════════ */

  @media (max-width: 850px) {
    .home-area {
      grid-template-columns: 1fr;
      gap: 0.5rem;
      padding: 1.3rem 0;
    }

    .home-area:first-child {
      padding-top: 1.4rem;
    }

    .home-joinus {
      grid-template-columns: 1fr;
    }

    .home-joinus-button {
      justify-self: start;
    }
  }

  @media (max-width: 520px) {
    .home-head,
    .post article > h2 {
      font-size: 1.4rem;
    }

    .home-head-ko,
    .post article > h2 > a::after {
      font-size: 0.88rem;
    }

    .home-joinus-button {
      width: 100%;
    }
  }

  @media (prefers-reduced-motion: reduce) {
    .home-joinus-button {
      transition: none;
    }
  }
</style>

<div markdown="0" class="home-brand" style="margin-bottom: 2rem;">
  <img
    src="/assets/img/Logo.png"
    alt="BioMolE Lab Logo"
    style="display: block; width: 100%; max-width: 230px; height: auto; background: #ffffff; padding: 0.6rem; border-radius: 6px;"
  >
  <div style="font-size: 1.05rem; color: var(--global-text-color-light); line-height: 1.5; margin-top: 0.9rem;">
    Dept. of Chem. Eng. &amp; Appl. Chem.<br>
    Chungnam National University
  </div>
</div>

<div style="font-size: 1.55rem; font-weight: 700; line-height: 1.3; color: var(--joinus-accent, #1a3a6b); margin-bottom: 0.5rem;">
  Designing Biomolecules. Engineering Biosystems.
</div>

<div style="font-size: 1.15rem; font-weight: 400; color: var(--global-text-color-light); line-height: 1.5; margin-bottom: 2rem;">
  From molecular interactions and biomolecular organization to catalysis, transport, and bioprocesses.
</div>

At the **BioMolE Lab**, we study how protein sequences and the resulting molecular interactions influence protein function, biomolecular condensate formation, and interfacial reorganization. We also examine how the resulting microenvironments affect molecular organization and enzyme activity.

Based on this understanding, we develop functional biomaterials and engineer enzymes for biocatalysis and bioprocess applications.

<p
  lang="ko"
  style="
    margin: 1.35rem 0 0;
    color: var(--global-text-color);
    font-size: 0.96rem;
    line-height: 1.8;
    word-break: keep-all;
  "
>
  충남대학교 생체분자공학연구실은 단백질 서열과 이에 따른 분자 간 상호작용이 단백질 기능, 생체분자 응축, 계면 재구성에 미치는 영향을 연구합니다.
  이를 바탕으로 기능성 생체소재와 생촉매를 개발하고, 생물공정 분야로 응용을 확장하고 있습니다.
</p>

<section markdown="0" class="home-research" aria-labelledby="home-research-title">
  <h2 class="home-head" id="home-research-title">
    Research<span class="home-head-ko" lang="ko">연구 분야</span>
  </h2>

  <div class="home-areas">
    <a class="home-area" href="{{ '/research/' | relative_url }}#condensates-biomaterials">
      <h3 class="home-area-title">
        Biomolecular Condensates &amp; Functional Biomaterials
      </h3>
      <p class="home-area-desc">
        How protein sequence and molecular interactions control coacervation,
        compartment formation, and interfacial organization.
      </p>
    </a>

    <a class="home-area" href="{{ '/research/' | relative_url }}#enzyme-engineering">
      <h3 class="home-area-title">
        Enzyme Discovery &amp; Engineering
      </h3>
      <p class="home-area-desc">
        Discovering and engineering enzymes for selective biocatalysis and
        compartmentalized reaction systems.
      </p>
    </a>

    <a class="home-area" href="{{ '/research/' | relative_url }}#biointerfaces-bioprocesses">
      <h3 class="home-area-title">
        Biointerfaces, Mass Transfer &amp; Bioprocess Engineering
      </h3>
      <p class="home-area-desc">
        Understanding transport limitations and engineering biological
        processes for improved performance.
      </p>
    </a>
  </div>

  <p class="home-research-more">
    <a href="{{ '/research/' | relative_url }}">All research areas</a>
  </p>
</section>

<section markdown="0" class="home-joinus" aria-labelledby="home-joinus-title">
  <div>
    <h2 class="home-joinus-title" id="home-joinus-title">
      We welcome prospective graduate and undergraduate researchers.
    </h2>

    <p class="home-joinus-text">
      Research topics, training, and application procedures are described on the Join&nbsp;Us page.<br>
      <span lang="ko">대학원생 및 학부연구생을 모집합니다.</span>
    </p>
  </div>

  <a class="home-joinus-button" href="{{ '/joinus/' | relative_url }}">
    Join Us
  </a>
</section>
