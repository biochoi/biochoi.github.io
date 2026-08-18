---
layout: page
title: People
permalink: /people/
description: Members of the BioMolE Lab at Chungnam National University.
nav: true
nav_order: 4
---

<style>
  /* Section headings */
  .ppl-head {
    display: flex;
    flex-wrap: wrap;
    align-items: baseline;
    gap: 0.35rem 0.65rem;
    clear: both;
    margin: 3.7rem 0 0;
    padding-bottom: 0.7rem;
    border-bottom: 2px solid var(--joinus-accent, #1a3a6b);
    color: var(--joinus-accent, #1a3a6b);
    font-size: 1.55rem;
    font-weight: 700;
    letter-spacing: -0.01em;
    line-height: 1.25;
  }

  .ppl-head:first-of-type {
    margin-top: 0.5rem;
  }

  .ppl-head-ko {
    color: var(--global-text-color-light);
    font-size: 0.93rem;
    font-weight: 400;
    letter-spacing: 0;
  }

  /* Principal Investigator */
  .ppl-pi {
    display: grid;
    grid-template-columns: 165px minmax(0, 1fr);
    gap: 1.8rem;
    align-items: start;
    margin: 2rem 0 1rem;
  }

  .ppl-pi-photo {
    display: block;
    width: 165px;
    height: 205px;
    border-radius: 8px;
    object-fit: cover;
    object-position: center 20%;
  }
  
  .ppl-pi-name {
    margin: 0 0 0.25rem;
    color: var(--joinus-accent, #1a3a6b);
    font-size: 1.28rem;
    font-weight: 700;
    line-height: 1.35;
  }

  .ppl-name-ko {
    margin-left: 0.4rem;
    color: var(--global-text-color-light);
    font-size: 0.86em;
    font-weight: 400;
  }

  .ppl-pi-role {
    margin: 0 0 1.05rem;
    color: var(--global-text-color-light);
    font-size: 0.94rem;
    line-height: 1.6;
  }

  .ppl-pi-bio {
    max-width: 680px;
    margin: 0 0 1.1rem;
    line-height: 1.75;
  }

  .ppl-pi-links {
    display: flex;
    flex-wrap: wrap;
    gap: 0.55rem 1.25rem;
    font-size: 0.9rem;
  }

  .ppl-pi-links a,
  .ppl-pi-links a:visited {
    color: var(--global-theme-color, #1a4d3e);
    font-weight: 650;
    text-decoration: none;
  }

  .ppl-pi-links a:hover,
  .ppl-pi-links a:focus-visible {
    text-decoration: underline;
    text-underline-offset: 4px;
  }

  /* Member grid: exactly four columns on desktop */
  .ppl-grid {
    display: grid;
    grid-template-columns: repeat(4, minmax(0, 1fr));
    gap: 2.4rem 1.45rem;
    margin: 2rem 0 1rem;
  }

  .ppl-member {
    min-width: 0;
  }

  .ppl-photo,
  .ppl-photo-blank {
    display: block;
    width: 100%;
    height: 215px;
    border-radius: 8px;
    object-fit: cover;
    background: var(--global-divider-color, #e8e8e8);
  }

  .ppl-photo-blank {
    display: flex;
    align-items: center;
    justify-content: center;
    color: var(--joinus-accent, #1a3a6b);
    font-size: 2rem;
    font-weight: 700;
  }

  .ppl-name {
    margin: 0.8rem 0 0.18rem;
    color: var(--joinus-accent, #1a3a6b);
    font-size: 0.98rem;
    font-weight: 700;
    line-height: 1.4;
  }

  .ppl-role {
    margin: 0;
    color: var(--global-text-color-light);
    font-size: 0.82rem;
    line-height: 1.5;
  }

  .ppl-joined {
    white-space: nowrap;
  }

  .ppl-topic {
    margin: 0.48rem 0 0;
    font-size: 0.84rem;
    line-height: 1.55;
  }

  /* Alumni */
  .ppl-alumni-wrap {
    width: 100%;
    margin: 1.8rem 0 1rem;
    overflow-x: auto;
  }

  .ppl-alumni {
    width: 100%;
    min-width: 720px;
    border-collapse: collapse;
    font-size: 0.88rem;
  }

  .ppl-alumni th,
  .ppl-alumni td {
    padding: 0.78rem 0.9rem 0.78rem 0;
    border-bottom: 1px solid var(--global-divider-color, #e0e0e0);
    text-align: left;
    vertical-align: top;
    line-height: 1.55;
  }

  .ppl-alumni th {
    color: var(--global-text-color-light);
    font-weight: 600;
    white-space: nowrap;
  }

  /* Join Us: no card or boxed button */
  .ppl-joinus {
    display: grid;
    grid-template-columns: minmax(0, 1fr) auto;
    align-items: center;
    gap: 1.2rem 2.5rem;
    margin: 3.7rem 0 2rem;
    padding: 1.6rem 0;
    border-top: 1px solid var(--global-divider-color, #e0e0e0);
    border-bottom: 1px solid var(--global-divider-color, #e0e0e0);
  }

  .ppl-joinus-title {
    margin: 0 0 0.35rem;
    color: var(--joinus-accent, #1a3a6b);
    font-size: 1.07rem;
    font-weight: 700;
    line-height: 1.45;
  }

  .ppl-joinus-text {
    margin: 0;
    color: var(--global-text-color-light);
    font-size: 0.92rem;
    line-height: 1.6;
  }

  .ppl-joinus-link,
  .ppl-joinus-link:visited {
    color: var(--global-theme-color, #1a4d3e);
    font-size: 0.94rem;
    font-weight: 700;
    text-decoration: none;
    white-space: nowrap;
  }

  .ppl-joinus-link:hover,
  .ppl-joinus-link:focus-visible {
    text-decoration: underline;
    text-underline-offset: 4px;
  }

  @media (max-width: 900px) {
    .ppl-grid {
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 2.1rem 1.3rem;
    }
  }

  @media (max-width: 700px) {
    .ppl-pi {
      grid-template-columns: 1fr;
      gap: 1.35rem;
    }

    .ppl-pi-photo {
      width: 150px;
      height: 185px;
    }

    .ppl-head {
      font-size: 1.38rem;
    }

    .ppl-joinus {
      grid-template-columns: 1fr;
    }
  }

  @media (max-width: 420px) {
    .ppl-grid {
      gap: 1.8rem 0.9rem;
    }

    .ppl-name {
      font-size: 0.93rem;
    }

    .ppl-topic {
      font-size: 0.8rem;
    }
  }
</style>

<h2 class="ppl-head">
  Principal Investigator
  <span class="ppl-head-ko" lang="ko">연구책임자</span>
</h2>

<section class="ppl-pi" aria-label="Principal Investigator">
  <img
    class="ppl-pi-photo"
    src="{{ '/assets/img/prof_pic.jpg' | relative_url }}"
    alt="Portrait of Prof. Yoo Seong Choi"
    width="800"
    height="1000"
  >

  <div>
    <p class="ppl-pi-name">
      Yoo Seong Choi
      <span class="ppl-name-ko" lang="ko">최유성</span>
    </p>

    <p class="ppl-pi-role">
      Professor, Department of Chemical Engineering and Applied Chemistry<br>
      Chungnam National University<br>
      <a href="mailto:biochoi@cnu.ac.kr">biochoi@cnu.ac.kr</a>
    </p>

    <p class="ppl-pi-bio">
      Prof. Choi's research examines how molecular interactions organize
      biomolecules and how these principles can be translated into functional
      biomaterials, biocatalysis, and bioprocesses. The laboratory integrates
      protein engineering, quantitative biophysics, synthetic biology, and
      bioprocess engineering.
    </p>

    <nav class="ppl-pi-links" aria-label="Principal investigator links">
      <a href="{{ '/research/' | relative_url }}">Research</a>
      <a href="{{ '/publications/' | relative_url }}">Publications</a>
      <a href="{{ '/contact/' | relative_url }}">Contact</a>
    </nav>
  </div>
</section>

{% assign grads = site.data.members.graduate %}
{% if grads and grads != empty %}
  <h2 class="ppl-head">
    Graduate Students
    <span class="ppl-head-ko" lang="ko">대학원생</span>
  </h2>

  <div class="ppl-grid">
    {% for m in grads %}
      <article class="ppl-member">
        {% if m.image %}
          <img
            class="ppl-photo"
            src="{{ '/assets/img/members/' | append: m.image | relative_url }}"
            alt="Portrait of {{ m.name_en }}"
            loading="lazy"
            decoding="async"
            width="800"
            height="1000"
            style="object-position: {{ m.photo_position | default: 'center 25%' }};"
          >
        {% else %}
          <div class="ppl-photo-blank" aria-hidden="true">
            {% if m.initials %}{{ m.initials }}{% else %}{{ m.name_en | slice: 0, 1 }}{% endif %}
          </div>
        {% endif %}

        <p class="ppl-name">
          {{ m.name_en }}{% if m.name_ko %}<span class="ppl-name-ko" lang="ko">{{ m.name_ko }}</span>{% endif %}
        </p>

        <p class="ppl-role">
          {{ m.role }}{% if m.joined %}<span class="ppl-joined"> · Joined {{ m.joined }}</span>{% endif %}
        </p>

        {% if m.topic %}<p class="ppl-topic">{{ m.topic }}</p>{% endif %}
      </article>
    {% endfor %}
  </div>
{% endif %}

{% assign undergrads = site.data.members.undergraduate %}
{% if undergrads and undergrads != empty %}
  <h2 class="ppl-head">
    Undergraduate Researchers
    <span class="ppl-head-ko" lang="ko">학부연구생</span>
  </h2>

  <div class="ppl-grid">
    {% for m in undergrads %}
      <article class="ppl-member">
        {% if m.image %}
          <img
            class="ppl-photo"
            src="{{ '/assets/img/members/' | append: m.image | relative_url }}"
            alt="Portrait of {{ m.name_en }}"
            loading="lazy"
            decoding="async"
            width="800"
            height="1000"
            style="object-position: {{ m.photo_position | default: 'center 25%' }};"
          >
        {% else %}
          <div class="ppl-photo-blank" aria-hidden="true">
            {% if m.initials %}{{ m.initials }}{% else %}{{ m.name_en | slice: 0, 1 }}{% endif %}
          </div>
        {% endif %}

        <p class="ppl-name">
          {{ m.name_en }}{% if m.name_ko %}<span class="ppl-name-ko" lang="ko">{{ m.name_ko }}</span>{% endif %}
        </p>

        <p class="ppl-role">
          {{ m.role }}{% if m.joined %}<span class="ppl-joined"> · Joined {{ m.joined }}</span>{% endif %}
        </p>

        {% if m.topic %}<p class="ppl-topic">{{ m.topic }}</p>{% endif %}
      </article>
    {% endfor %}
  </div>
{% endif %}

{% assign alumni = site.data.members.alumni %}
{% if alumni and alumni != empty %}
  <h2 class="ppl-head">
    Alumni
    <span class="ppl-head-ko" lang="ko">졸업생</span>
  </h2>

  <div class="ppl-alumni-wrap">
    <table class="ppl-alumni">
      <thead>
        <tr>
          <th scope="col">Year</th>
          <th scope="col">Name</th>
          <th scope="col">Degree</th>
          <th scope="col">Thesis</th>
          <th scope="col">Current position</th>
        </tr>
      </thead>
      <tbody>
        {% for a in alumni %}
          <tr>
            <td>{{ a.year }}</td>
            <td>
              {{ a.name_en }}{% if a.name_ko %} <span lang="ko">{{ a.name_ko }}</span>{% endif %}
            </td>
            <td>{{ a.degree | default: '—' }}</td>
            <td>{{ a.thesis | default: '—' }}</td>
            <td>{{ a.position | default: '—' }}</td>
          </tr>
        {% endfor %}
      </tbody>
    </table>
  </div>
{% endif %}

<section class="ppl-joinus" aria-label="Join the BioMolE Lab">
  <div>
    <p class="ppl-joinus-title">
      We welcome prospective graduate and undergraduate researchers.
    </p>
    <p class="ppl-joinus-text">
      Research topics, training, and application procedures are described on the Join&nbsp;Us page.<br>
      <span lang="ko">대학원생 및 학부연구생 지원 안내는 Join Us 페이지에서 확인할 수 있습니다.</span>
    </p>
  </div>

  <a class="ppl-joinus-link" href="{{ '/joinus/' | relative_url }}">
    Join Us <span aria-hidden="true">→</span>
  </a>
</section>

