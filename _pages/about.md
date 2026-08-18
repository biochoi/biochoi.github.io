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
    <p>E-mail: biochoi@cnu.ac.kr</p>
    <p>Engineering Bldg. 1, Room 152, Chungnam National University</p>
    <p>99 Daehak-ro, Yuseong-gu, Daejeon 34134, Republic of Korea</p>

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
  @media (min-width: 768px) {
    .profile {
      margin-top: 3rem;
    }
  }

  /* ══════════════════════════════════════════════════════════
   * 공통 섹션 제목
   *   .home-section-heading  → 본문에 직접 작성한 Research 제목
   *   .post article > h2     → 테마가 자동 생성하는 News /
   *                            Selected publications 제목
   * 두 가지가 같은 모양을 갖도록 규칙을 공유합니다.
   * ══════════════════════════════════════════════════════════ */

  .home-section-heading,
  .post article > h2 {
    clear: both;
    max-width: none;
    margin: 3.75rem 0 1.7rem;
    text-align: left;
  }

  .home-section-heading h2,
  .post article > h2 {
    color: var(--joinus-accent, #1a3a6b);
    font-size: 1.85rem;
    font-weight: 700;
    line-height: 1.2;
  }

  .home-section-heading h2 {
    margin: 0;
  }

  /* 테마가 만든 제목은 소문자라 첫 글자를 대문자로 맞춥니다. */
  .post article > h2 {
    text-transform: capitalize;
  }

  .post article > h2 > a {
    display: inline-block;
    text-decoration: none;
  }

  /* 국문 부제 */
  .home-section-heading p,
  .post article > h2 > a::after {
    display: block;
    margin: 0.4rem 0 0;
    color: var(--global-text-color-light);
    font-size: 1rem;
    font-weight: 400;
    line-height: 1.4;
    text-transform: none;
  }

  .post article > h2 > a[href$="/news/"]::after {
    content: "소식";
  }

  .post article > h2 > a[href$="/publications/"]::after {
    content: "대표 논문";
  }

  /* 제목 아래 짧은 강조선 */
  .home-section-heading::after,
  .post article > h2::after {
    display: block;
    width: 44px;
    height: 3px;
    margin: 1rem 0 0;
    border-radius: 999px;
    background: var(--global-theme-color, #1a4d3e);
    content: "";
  }

  /* ══════════════════════════════════════════════════════════
   * Research 카드
   * ══════════════════════════════════════════════════════════ */

  .home-research-section {
    clear: both;
    width: 100%;
    margin: 3.75rem 0 3rem;
  }

  .home-research-grid {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 1.1rem;
    width: 100%;
    margin: 0;
  }

  .home-research-card,
  .home-research-card:visited {
    display: flex;
    flex-direction: column;
    min-width: 0;
    box-sizing: border-box;
    padding: 1.3rem 1.2rem 1.2rem;
    border: 1px solid var(--global-divider-color, #e0e0e0);
    border-top: 4px solid var(--joinus-line, #1a3a6b);
    border-radius: 10px;
    background: var(--global-card-bg-color, transparent);
    color: var(--global-text-color);
    text-decoration: none;
    transition:
      transform 0.18s ease,
      border-color 0.18s ease,
      box-shadow 0.18s ease;
  }

  .home-research-card:hover,
  .home-research-card:focus-visible {
    border-color: var(--joinus-line, #1a3a6b);
    box-shadow: 0 10px 24px rgba(0, 0, 0, 0.08);
    color: var(--global-text-color);
    text-decoration: none;
    transform: translateY(-3px);
  }

  .home-research-card:focus-visible {
    outline: 3px solid rgba(26, 77, 62, 0.25);
    outline-offset: 3px;
  }

  .home-card-number {
    margin-bottom: 0.7rem;
    color: var(--global-theme-color, #1a4d3e);
    font-size: 0.74rem;
    font-weight: 700;
    letter-spacing: 0.1em;
  }

  .home-card-title {
    min-height: 4.1rem;
    margin: 0 0 0.65rem;
    color: var(--joinus-accent, #1a3a6b);
    font-size: 1.03rem;
    font-weight: 700;
    line-height: 1.35;
  }

  .home-card-desc {
    margin: 0 0 1rem;
    color: var(--global-text-color-light);
    font-size: 0.91rem;
    line-height: 1.58;
  }

  .home-card-more {
    margin-top: auto;
    padding-top: 0.8rem;
    border-top: 1px solid var(--global-divider-color, #e0e0e0);
    color: var(--global-theme-color, #1a4d3e);
    font-size: 0.86rem;
    font-weight: 700;
  }

  .home-research-card:hover .home-card-more {
    text-decoration: underline;
    text-underline-offset: 3px;
  }

  .home-research-footer {
    margin-top: 1.3rem;
    text-align: left;
  }

  .home-research-link {
    color: var(--global-theme-color, #1a4d3e);
    font-size: 0.94rem;
    font-weight: 700;
    text-decoration: none;
  }

  .home-research-link:hover {
    text-decoration: underline;
    text-underline-offset: 4px;
  }

  /* ══════════════════════════════════════════════════════════
   * News / Selected publications 본문 여백
   * ══════════════════════════════════════════════════════════ */

  .post article > .news,
  .post article > .publications {
    margin-bottom: 3rem;
  }

  /* ══════════════════════════════════════════════════════════
   * Join Us 배너
   * ══════════════════════════════════════════════════════════ */

  .home-joinus-panel {
    clear: both;
    display: grid;
    grid-template-columns: minmax(0, 1fr) auto;
    align-items: center;
    gap: 1.5rem;
    width: 100%;
    box-sizing: border-box;
    margin: 0 0 3rem;
    padding: 1.5rem 1.6rem;
    border: 1px solid var(--global-divider-color, #e0e0e0);
    border-top: 4px solid var(--global-theme-color, #1a4d3e);
    border-radius: 12px;
    background: var(--global-card-bg-color, transparent);
    box-shadow: 0 8px 22px rgba(0, 0, 0, 0.05);
  }

  .home-joinus-kicker {
    margin-bottom: 0.35rem;
    color: var(--global-theme-color, #1a4d3e);
    font-size: 0.74rem;
    font-weight: 800;
    letter-spacing: 0.1em;
    text-transform: uppercase;
  }

  .home-joinus-title {
    margin: 0 0 0.4rem;
    color: var(--joinus-accent, #1a3a6b);
    font-size: 1.18rem;
    font-weight: 700;
    line-height: 1.35;
  }

  .home-joinus-text {
    margin: 0;
    color: var(--global-text-color-light);
    font-size: 0.95rem;
    line-height: 1.55;
  }

  .home-joinus-button,
  .home-joinus-button:visited {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    min-height: 44px;
    padding: 0.72rem 1.1rem;
    border: 2px solid var(--global-theme-color, #1a4d3e);
    border-radius: 999px;
    background: var(--global-theme-color, #1a4d3e);
    color: #ffffff;
    font-size: 0.91rem;
    font-weight: 700;
    line-height: 1.2;
    text-decoration: none;
    white-space: nowrap;
    transition:
      transform 0.18s ease,
      box-shadow 0.18s ease;
  }

  .home-joinus-button:hover,
  .home-joinus-button:focus-visible {
    box-shadow: 0 8px 18px rgba(0, 0, 0, 0.14);
    color: #ffffff;
    text-decoration: none;
    transform: translateY(-2px);
  }

  .home-joinus-button:focus-visible {
    outline: 3px solid rgba(26, 77, 62, 0.25);
    outline-offset: 3px;
  }

  /* ══════════════════════════════════════════════════════════
   * 반응형
   * ══════════════════════════════════════════════════════════ */

  @media (max-width: 900px) {
    .home-research-grid {
      grid-template-columns: 1fr;
    }

    .home-card-title {
      min-height: 0;
    }

    .home-joinus-panel {
      grid-template-columns: 1fr;
    }

    .home-joinus-button {
      justify-self: start;
    }
  }

  @media (max-width: 520px) {
    .home-research-section {
      margin-top: 3rem;
    }

    .home-section-heading h2,
    .post article > h2 {
      font-size: 1.65rem;
    }

    .home-joinus-panel {
      padding: 1.3rem 1.15rem;
    }

    .home-joinus-button {
      width: 100%;
    }
  }

  @media (prefers-reduced-motion: reduce) {
    .home-research-card,
    .home-joinus-button {
      transition: none;
    }
  }
</style>

<div markdown="0" style="display: flex; flex-wrap: wrap; align-items: center; gap: 1.5rem; margin-bottom: 2rem;">
  <img
    src="/assets/img/Logo.png"
    alt="BioMolE Lab Logo"
    style="width: 100%; max-width: 230px; height: auto; background: #ffffff; padding: 0.6rem; border-radius: 6px;"
  >
  <div style="font-size: 1.05rem; color: var(--global-text-color-light); line-height: 1.5; flex: 1; min-width: 12rem;">
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

At the **BioMolE Lab**, we study and engineer biological function at multiple levels—from protein sequences and molecular interactions to biomolecular assemblies, cells, and bioprocesses. We investigate how sequence-dependent molecular interactions drive coacervation, phase separation, and interfacial reorganization, and how the resulting microenvironments affect biomolecular organization and catalytic activity. We also discover and engineer enzymes for biocatalysis and examine how interfacial and mass-transfer processes influence biological systems and bioprocess performance.

By combining protein engineering, quantitative biophysics, synthetic biology, and bioprocess engineering, we develop biomolecular platforms for functional biomaterials and biocatalysis and improve bioprocess efficiency. Our goal is to understand the underlying mechanisms, use that knowledge for rational design, and develop useful technologies.

<section markdown="0" class="home-research-section" aria-labelledby="home-research-title">
  <div class="home-section-heading">
    <h2 id="home-research-title">Research</h2>
    <p lang="ko">연구 분야</p>
  </div>

  <div class="home-research-grid">
    <a
      class="home-research-card"
      href="{{ '/research/' | relative_url }}#condensates-biomaterials"
    >
      <span class="home-card-number">RESEARCH 01</span>
      <h3 class="home-card-title">
        Biomolecular Condensates &amp; Functional Biomaterials
      </h3>
      <p class="home-card-desc">
        How protein sequence and molecular interactions control coacervation,
        compartment formation, and interfacial organization.
      </p>
      <span class="home-card-more">
        Explore this area <span aria-hidden="true">&rarr;</span>
      </span>
    </a>

    <a
      class="home-research-card"
      href="{{ '/research/' | relative_url }}#enzyme-engineering"
    >
      <span class="home-card-number">RESEARCH 02</span>
      <h3 class="home-card-title">
        Enzyme Discovery &amp; Engineering
      </h3>
      <p class="home-card-desc">
        Discovering and engineering enzymes for selective biocatalysis,
        biomaterials, and sensing.
      </p>
      <span class="home-card-more">
        Explore this area <span aria-hidden="true">&rarr;</span>
      </span>
    </a>

    <a
      class="home-research-card"
      href="{{ '/research/' | relative_url }}#biointerfaces-bioprocesses"
    >
      <span class="home-card-number">RESEARCH 03</span>
      <h3 class="home-card-title">
        Biointerfaces, Mass Transfer &amp; Bioprocess Engineering
      </h3>
      <p class="home-card-desc">
        Understanding transport limitations and engineering biological
        processes for improved performance.
      </p>
      <span class="home-card-more">
        Explore this area <span aria-hidden="true">&rarr;</span>
      </span>
    </a>
  </div>

  <div class="home-research-footer">
    <a
      class="home-research-link"
      href="{{ '/research/' | relative_url }}"
    >
      View all research <span aria-hidden="true">&rarr;</span>
    </a>
  </div>
</section>

<section markdown="0" class="home-joinus-panel" aria-labelledby="home-joinus-title">
  <div>
    <div class="home-joinus-kicker">
      Join the BioMolE Lab
    </div>

    <h2 class="home-joinus-title" id="home-joinus-title">
      Interested in conducting research with us?
    </h2>

    <p class="home-joinus-text">
      We welcome inquiries from prospective graduate and undergraduate researchers.
    </p>
  </div>

  <a
    class="home-joinus-button"
    href="{{ '/joinus/' | relative_url }}"
  >
    Join Us <span aria-hidden="true">&rarr;</span>
  </a>
</section>
