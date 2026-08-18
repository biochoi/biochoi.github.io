---
layout: page
title: Contact
permalink: /contact/
description: Contact information and directions to the BioMolE Lab at Chungnam National University.
nav: true
nav_order: 6
---

<style>
  .contact-lead {
    margin-bottom: 2rem;
    line-height: 1.8;
  }

  .contact-grid {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 1.2rem;
    margin: 1.5rem 0 1rem;
  }

  .contact-card {
    padding: 1.4rem;
    border: 1px solid var(--global-divider-color);
    border-radius: 10px;
    background-color: var(--global-card-bg-color);
  }

  .contact-card h2 {
    margin-top: 0;
    margin-bottom: 1rem;
    font-size: 1.25rem;
  }

  .contact-card p {
    line-height: 1.75;
  }

  .contact-card p:last-child {
    margin-bottom: 0;
  }

  /* ── 아래 섹션 전용 여백 ───────────────────────── */

  .contact-directions {
    margin-top: 3.5rem;
    padding-top: 2.5rem;
    border-top: 1px solid var(--global-divider-color);
  }

  .contact-directions h2 {
    margin-top: 0;
    margin-bottom: 1.5rem;
    line-height: 1.35;
  }

  .contact-directions p {
    margin-bottom: 1.2rem;
    line-height: 1.8;
  }

  .contact-building {
    margin-bottom: 1.8rem;
  }

  /* 국문 안내와 영문 안내 사이를 넉넉히 벌려 덩어리를 분리 */
  .contact-directions p[lang="ko"] {
    margin-bottom: 1.8rem;
  }

  .contact-actions {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
    gap: 0.8rem;
    margin: 2.2rem 0 2.6rem;
  }

  .contact-button {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    min-height: 44px;
    padding: 0.75rem 0.7rem;
    border: 2px solid var(--global-theme-color);
    border-radius: 8px;
    color: var(--global-theme-color);
    font-weight: 600;
    line-height: 1.35;
    text-align: center;
    text-decoration: none;
    transition:
      background-color 0.2s ease,
      color 0.2s ease,
      transform 0.2s ease;
  }

  .contact-button:hover,
  .contact-button:focus-visible {
    background-color: var(--global-theme-color);
    color: var(--global-hover-text-color);
    text-decoration: none;
    transform: translateY(-2px);
  }

  .contact-button:focus-visible {
    outline: 2px solid var(--global-theme-color);
    outline-offset: 3px;
  }

  .contact-note {
    margin-top: 0;
    padding: 1.3rem 1.4rem;
    border-left: 4px solid var(--global-theme-color);
    border-radius: 0 8px 8px 0;
    background-color: var(--global-card-bg-color);
    line-height: 1.8;
  }

  .contact-note p {
    margin-bottom: 0;
  }

  .contact-footnote {
    margin-top: 3.2rem;
    padding-top: 2rem;
    margin-bottom: 2rem;
    border-top: 1px solid var(--global-divider-color);
    line-height: 1.8;
  }

  @media (max-width: 700px) {
    .contact-grid {
      grid-template-columns: 1fr;
    }

    .contact-directions {
      margin-top: 2.6rem;
      padding-top: 2rem;
    }
  }
</style>

<p class="contact-lead">
  BioMolE Lab은 충남대학교 대덕캠퍼스 공과대학 1호관(W3)에 있습니다.<br>
  The BioMolE Lab is located in College of Engineering I (W3) on the Daedeok Campus of Chungnam National University.
</p>

<div class="contact-grid">
  <section class="contact-card" aria-labelledby="pi-heading">
    <h2 id="pi-heading">Principal Investigator</h2>

    <p>
      <strong>Prof. Yoo Seong Choi</strong><br>
      Department of Chemical Engineering and Applied Chemistry<br>
      Chungnam National University
    </p>

    <p>
      <strong>E-mail:</strong>
      <a href="mailto:biochoi@cnu.ac.kr">biochoi@cnu.ac.kr</a><br>
      <strong>Phone:</strong> +82-42-821-5682
    </p>
  </section>

  <section class="contact-card" aria-labelledby="address-heading">
    <h2 id="address-heading">Address | 주소</h2>

    <p lang="ko">
      <strong>국문</strong><br>
      충남대학교 공과대학 1호관(W3) 152호<br>
      대전광역시 유성구 대학로 99<br>
      우편번호 34134
    </p>

    <p>
      <strong>English</strong><br>
      Room 152, College of Engineering I (W3)<br>
      Chungnam National University<br>
      99 Daehak-ro, Yuseong-gu<br>
      Daejeon 34134, Republic of Korea
    </p>
  </section>
</div>

<section class="contact-directions" aria-labelledby="directions-heading">
  <h2 id="directions-heading">Campus Map &amp; Directions | 캠퍼스 안내</h2>

  <p class="contact-building">
    <strong>Building code:</strong> W3 — College of Engineering I (공과대학 1호관)
  </p>

  <p lang="ko">
    교내에서는 공식 캠퍼스 안내도에서 <strong>W3</strong>를 찾거나, 지도 앱에서
    <strong>“충남대학교 공과대학 1호관”</strong>을 검색해 주세요.
  </p>

  <p>
    On campus, look for <strong>W3 (College of Engineering I)</strong> on the official campus map
    or search for <strong>“Chungnam National University College of Engineering I”</strong>
    in a map application.
  </p>

  <div class="contact-actions">
    <a class="contact-button"
       href="https://plus.cnu.ac.kr/html/kr/sub01/sub01_010804.html"
       target="_blank"
       rel="noopener noreferrer">
      CNU Campus Map ↗
    </a>

    <a class="contact-button"
       href="https://plus.cnu.ac.kr/html/kr/sub01/sub01_01080302.html"
       target="_blank"
       rel="noopener noreferrer">
      Transportation Guide ↗
    </a>

    <a class="contact-button"
       href="https://www.google.com/maps/search/?api=1&amp;query=Chungnam+National+University+College+of+Engineering+I"
       target="_blank"
       rel="noopener noreferrer">
      Google Maps ↗
    </a>

    <a class="contact-button"
       href="https://plus.cnu.ac.kr/html/kr/sub05/sub05_05040201.html"
       target="_blank"
       rel="noopener noreferrer">
      Parking Information ↗
    </a>
  </div>

  <div class="contact-note">
    <p>
      <strong>Visitor Information | 방문 안내</strong><br>
      방문 일정은 사전에 연구실과 조율해 주세요. 차량 방문자는 출발 전에 충남대학교 공식 주차 안내를 확인하시기 바랍니다.<br>
      Please arrange your visit in advance and check the official parking information before arriving by car.
    </p>
  </div>

  <p class="contact-footnote">
    Prospective students should review the
    <a href="{{ '/joinus/' | relative_url }}">Join Us</a>
    page before contacting the laboratory.
  </p>
</section>
