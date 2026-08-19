---
layout: page
title: People
permalink: /people/
description: Members of the BioMolE Lab at Chungnam National University.
nav: true
nav_order: 4
---

<style>

  /* People page quick navigation */
  .ppl-jump-nav {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    gap: 0.55rem 1.15rem;
    margin: 0.25rem 0 2.35rem;
    padding: 0.9rem 0;
    border-top: 1px solid var(--global-divider-color, #e0e0e0);
    border-bottom: 1px solid var(--global-divider-color, #e0e0e0);
  }

  .ppl-jump-label {
    color: var(--global-text-color-light);
    font-size: 0.7rem;
    font-weight: 700;
    letter-spacing: 0.075em;
    line-height: 1.4;
    text-transform: uppercase;
  }

  .ppl-jump-nav a,
  .ppl-jump-nav a:visited {
    color: var(--global-theme-color, #1a4d3e);
    font-size: 0.87rem;
    font-weight: 600;
    line-height: 1.45;
    text-decoration: none;
    white-space: nowrap;
  }

  .ppl-jump-nav a:hover,
  .ppl-jump-nav a:focus-visible {
    text-decoration: underline;
    text-underline-offset: 4px;
  }

  .ppl-anchor {
    scroll-margin-top: 6.5rem;
  }

  /* Top-level section headings */
  .ppl-head {
    display: flex;
    flex-wrap: wrap;
    align-items: baseline;
    gap: 0.35rem 0.65rem;
    clear: both;
    margin: 3.9rem 0 0;
    padding-bottom: 0.72rem;
    border-bottom: 2px solid var(--joinus-accent, #1a3a6b);
    color: var(--joinus-accent, #1a3a6b);
    font-size: 1.55rem;
    font-weight: 700;
    letter-spacing: -0.01em;
    line-height: 1.25;
  }

  .ppl-head-first {
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
    grid-template-columns: 175px minmax(0, 1fr);
    gap: 1.9rem;
    align-items: start;
    margin: 2.1rem 0 1rem;
  }

  .ppl-pi-photo-wrap {
    width: 175px;
    height: 220px;
    overflow: hidden;
    border-radius: 8px;
  }

  .ppl-pi-photo {
    display: block;
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: center 18%;
  }

  .ppl-pi-name {
    margin: 0 0 0.28rem;
    color: var(--joinus-accent, #1a3a6b);
    font-size: 1.3rem;
    font-weight: 700;
    line-height: 1.35;
  }

  .ppl-name-ko {
    margin-left: 0.42rem;
    color: var(--global-text-color-light);
    font-size: 0.86em;
    font-weight: 400;
  }

  .ppl-pi-role {
    margin: 0 0 1.05rem;
    color: var(--global-text-color-light);
    font-size: 0.94rem;
    line-height: 1.62;
  }

  .ppl-pi-bio {
    max-width: 700px;
    margin: 0 0 1.12rem;
    line-height: 1.75;
  }

  .ppl-pi-links {
    display: flex;
    flex-wrap: wrap;
    gap: 0.55rem 1.3rem;
    font-size: 0.9rem;
  }

  .ppl-pi-links a,
  .ppl-pi-links a:visited {
    color: var(--global-theme-color, #1a4d3e);
    font-weight: 600;
    text-decoration: none;
  }

  .ppl-pi-links a:hover,
  .ppl-pi-links a:focus-visible {
    text-decoration: underline;
    text-underline-offset: 4px;
  }

  /* PI profile details: collapsed by default so the team appears earlier */
  .ppl-profile-block {
    margin: 2.15rem 0 0.75rem;
    border-top: 1px solid var(--global-divider-color, #e0e0e0);
    border-bottom: 1px solid var(--global-divider-color, #e0e0e0);
  }

  .ppl-profile-summary {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 1.25rem;
    padding: 1rem 0;
    cursor: pointer;
    list-style: none;
  }

  .ppl-profile-summary::-webkit-details-marker {
    display: none;
  }

  .ppl-profile-summary::after {
    flex: 0 0 auto;
    color: var(--global-theme-color, #1a4d3e);
    content: "View details  +";
    font-size: 0.78rem;
    font-weight: 700;
    letter-spacing: 0.015em;
    white-space: nowrap;
  }

  .ppl-profile-block[open] .ppl-profile-summary::after {
    content: "Hide details  −";
  }

  .ppl-profile-label {
    display: flex;
    flex-wrap: wrap;
    align-items: baseline;
    gap: 0.35rem 0.55rem;
    margin: 0;
    color: var(--global-theme-color, #1a4d3e);
    font-size: 0.76rem;
    font-weight: 800;
    letter-spacing: 0.085em;
    line-height: 1.4;
    text-transform: uppercase;
  }

  .ppl-profile-label-ko {
    color: var(--global-text-color-light);
    font-size: 0.84rem;
    font-weight: 400;
    letter-spacing: 0;
    text-transform: none;
  }

  .ppl-cv {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 0 3rem;
    align-items: start;
    padding: 0.75rem 0 1.65rem;
  }

  .ppl-cv-column {
    display: flex;
    min-width: 0;
    flex-direction: column;
    gap: 2.05rem;
  }

  .ppl-cv-section h3 {
    margin: 0 0 1rem;
    padding-bottom: 0.52rem;
    border-bottom: 1px solid var(--global-divider-color, #e0e0e0);
    color: var(--global-text-color, #222222);
    font-size: 1rem;
    font-weight: 700;
    line-height: 1.45;
  }

  .ppl-cv-ko {
    margin-left: 0.45rem;
    color: var(--global-text-color-light);
    font-size: 0.83rem;
    font-weight: 400;
  }

  .ppl-cv-section ul {
    margin: 0;
    padding: 0;
    list-style: none;
  }

  .ppl-cv-section li {
    margin-bottom: 0.92rem;
  }

  .ppl-cv-section li:last-child {
    margin-bottom: 0;
  }

  .ppl-cv-when {
    display: block;
    margin-bottom: 0.1rem;
    color: var(--global-text-color-light);
    font-size: 0.77rem;
    font-variant-numeric: tabular-nums;
    letter-spacing: 0.015em;
  }

  .ppl-cv-what {
    display: block;
    color: var(--global-text-color, #222222);
    font-size: 0.89rem;
    font-weight: 600;
    line-height: 1.46;
  }

  .ppl-cv-where {
    display: block;
    margin-top: 0.08rem;
    color: var(--global-text-color-light);
    font-size: 0.83rem;
    line-height: 1.52;
  }

  /* Students: spacious two-column profiles */
  .ppl-grid {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 3rem 2.5rem;
    margin: 2.35rem 0 1.15rem;
  }

  .ppl-member {
    display: grid;
    grid-template-columns: 155px minmax(0, 1fr);
    gap: 1.25rem;
    align-items: start;
    min-width: 0;
    padding-bottom: 1.8rem;
    border-bottom: 1px solid var(--global-divider-color, #e0e0e0);
  }

  .ppl-photo,
  .ppl-photo-blank {
    display: block;
    width: 100%;
    aspect-ratio: 4 / 5;
    border-radius: 8px;
    object-fit: cover;
    background: var(--global-divider-color, #e8e8e8);
  }

  .ppl-photo {
    height: auto;
  }

  .ppl-photo-blank {
    display: flex;
    align-items: center;
    justify-content: center;
    color: var(--joinus-accent, #1a3a6b);
    font-size: 2rem;
    font-weight: 700;
  }

  .ppl-member-copy {
    min-width: 0;
    padding-top: 0.03rem;
  }

  .ppl-name {
    margin: 0 0 0.3rem;
    color: var(--joinus-accent, #1a3a6b);
    font-size: 1.08rem;
    font-weight: 700;
    line-height: 1.42;
  }

  .ppl-role {
    margin: 0;
    color: var(--global-text-color-light);
    font-size: 0.86rem;
    line-height: 1.55;
  }

  .ppl-joined {
    white-space: nowrap;
  }

  .ppl-topic {
    margin: 1rem 0 0;
    font-size: 0.9rem;
    line-height: 1.66;
  }

  .ppl-topic-label {
    display: block;
    margin-bottom: 0.25rem;
    color: var(--global-theme-color, #1a4d3e);
    font-size: 0.7rem;
    font-weight: 700;
    letter-spacing: 0.065em;
    line-height: 1.35;
    text-transform: uppercase;
  }

  /* Shared student workspace and telephone */
  .ppl-shared-contact {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 1.2rem 3rem;
    margin: 3rem 0 0.8rem;
    padding: 1.35rem 0;
    border-top: 1px solid var(--global-divider-color, #e0e0e0);
    border-bottom: 1px solid var(--global-divider-color, #e0e0e0);
  }

  .ppl-shared-contact-item {
    min-width: 0;
  }

  .ppl-shared-contact-label {
    display: block;
    margin-bottom: 0.35rem;
    color: var(--joinus-accent, #1a3a6b);
    font-size: 0.9rem;
    font-weight: 700;
    line-height: 1.42;
  }

  .ppl-shared-contact-ko {
    margin-left: 0.38rem;
    color: var(--global-text-color-light);
    font-size: 0.82rem;
    font-weight: 400;
  }

  .ppl-shared-contact-value {
    margin: 0;
    color: var(--global-text-color-light);
    font-size: 0.9rem;
    line-height: 1.62;
  }

  .ppl-shared-contact-value a,
  .ppl-shared-contact-value a:visited {
    color: var(--global-theme-color, #1a4d3e);
    font-weight: 600;
    text-decoration: none;
  }

  .ppl-shared-contact-value a:hover,
  .ppl-shared-contact-value a:focus-visible {
    text-decoration: underline;
    text-underline-offset: 3px;
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

  /* Join Us */
  .ppl-joinus {
    display: grid;
    grid-template-columns: minmax(0, 1fr) auto;
    align-items: center;
    gap: 1.2rem 2.5rem;
    margin: 3.8rem 0 2rem;
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
    line-height: 1.62;
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

  @media (max-width: 980px) {
    .ppl-grid {
      grid-template-columns: 1fr;
      gap: 2.35rem;
    }

    .ppl-member {
      grid-template-columns: 175px minmax(0, 1fr);
    }
  }

  @media (max-width: 720px) {
    .ppl-jump-nav {
      gap: 0.55rem 1rem;
      margin-bottom: 2rem;
    }

    .ppl-jump-label {
      width: 100%;
    }

    .ppl-profile-summary {
      align-items: flex-start;
    }

    .ppl-profile-summary::after {
      padding-top: 0.08rem;
    }

    .ppl-pi {
      grid-template-columns: 1fr;
      gap: 1.35rem;
    }

    .ppl-pi-photo-wrap {
      width: 160px;
      height: 200px;
    }

    .ppl-head {
      font-size: 1.38rem;
    }

    .ppl-cv {
      grid-template-columns: 1fr;
      gap: 2rem;
    }

    .ppl-shared-contact {
      grid-template-columns: 1fr;
      gap: 1.15rem;
    }

    .ppl-joinus {
      grid-template-columns: 1fr;
    }
  }

  @media (max-width: 560px) {
    .ppl-member {
      grid-template-columns: 125px minmax(0, 1fr);
      gap: 1rem;
    }

    .ppl-name {
      font-size: 1rem;
    }

    .ppl-topic {
      margin-top: 0.78rem;
      font-size: 0.86rem;
    }
  }

  @media (max-width: 420px) {
    .ppl-grid {
      gap: 2.15rem;
    }

    .ppl-member {
      grid-template-columns: 1fr;
      gap: 0.95rem;
    }

    .ppl-photo,
    .ppl-photo-blank {
      width: min(220px, 72vw);
    }
  }
</style>

{% assign grads = site.data.members.graduate %}
{% assign undergrads = site.data.members.undergraduate %}
{% assign alumni = site.data.members.alumni %}
{% assign shared_contact = site.data.members.shared_contact %}

<nav class="ppl-jump-nav" aria-label="People page navigation">
  <span class="ppl-jump-label">Jump to</span>

  <a href="#ppl-pi-heading">Principal Investigator</a>

  {% if grads and grads != empty %}
    <a href="#ppl-graduate-heading">Graduate Students</a>
  {% endif %}

  {% if undergrads and undergrads != empty %}
    <a href="#ppl-undergraduate-heading">Undergraduate Researchers</a>
  {% endif %}
</nav>

<section aria-labelledby="ppl-pi-heading">
  <h2 class="ppl-head ppl-head-first ppl-anchor" id="ppl-pi-heading">
    Principal Investigator
    <span class="ppl-head-ko" lang="ko">연구책임자</span>
  </h2>

  <div class="ppl-pi">
    <div class="ppl-pi-photo-wrap">
      <img
        class="ppl-pi-photo"
        src="{{ '/assets/img/prof_pic.jpg' | relative_url }}"
        alt="Portrait of Prof. Yoo Seong Choi"
        width="800"
        height="1000"
      >
    </div>

    <div>
      <p class="ppl-pi-name">
        Yoo Seong Choi
        <span class="ppl-name-ko" lang="ko">최유성</span>
      </p>

      <p class="ppl-pi-role">
        Professor, Department of Chemical Engineering and Applied Chemistry<br>
        Chungnam National University
      </p>

      <p class="ppl-pi-bio">
        Prof. Choi’s research focuses mainly on proteins and how their sequences,
        structures, and interactions shape assembly and function. His major research
        area include biomolecular condensates and enzyme engineering, with
        applications in functional biomaterials and bioprocesses.
       </p>

      <nav class="ppl-pi-links" aria-label="Principal investigator links">
        <a href="{{ '/research/' | relative_url }}">Research</a>
        <a href="{{ '/publications/' | relative_url }}">Publications</a>
        <a href="{{ '/contact/' | relative_url }}">Contact</a>
      </nav>
    </div>
  </div>

  {% assign cv_columns = site.data.pi_cv.columns %}
  {% if cv_columns and cv_columns != empty %}
    <details class="ppl-profile-block" id="ppl-selected-profile">
      <summary class="ppl-profile-summary">
        <span class="ppl-profile-label">
          Selected Profile
          <span class="ppl-profile-label-ko" lang="ko">주요 이력</span>
        </span>
      </summary>

      <div class="ppl-cv">
        {% for column in cv_columns %}
          <div class="ppl-cv-column">
            {% for sec in column.sections %}
              <section class="ppl-cv-section">
                <h3>
                  {{ sec.title }}{% if sec.title_ko %}<span class="ppl-cv-ko" lang="ko">{{ sec.title_ko }}</span>{% endif %}
                </h3>

                <ul>
                  {% for item in sec.items %}
                    <li>
                      {% if item.when %}<span class="ppl-cv-when">{{ item.when }}</span>{% endif %}
                      <span class="ppl-cv-what">{{ item.what }}</span>
                      {% if item.where %}<span class="ppl-cv-where">{{ item.where }}</span>{% endif %}
                    </li>
                  {% endfor %}
                </ul>
              </section>
            {% endfor %}
          </div>
        {% endfor %}
      </div>
    </details>
  {% endif %}
</section>

{% if grads and grads != empty %}
  <section aria-labelledby="ppl-graduate-heading">
    <h2 class="ppl-head ppl-anchor" id="ppl-graduate-heading">
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
              width="600"
              height="750"
              style="object-position: {{ m.photo_position | default: 'center 25%' }};"
            >
          {% else %}
            <div class="ppl-photo-blank" aria-hidden="true">
              {% if m.initials %}{{ m.initials }}{% else %}{{ m.name_en | slice: 0, 1 }}{% endif %}
            </div>
          {% endif %}

          <div class="ppl-member-copy">
            <h3 class="ppl-name">
              {{ m.name_en }}{% if m.name_ko %}<span class="ppl-name-ko" lang="ko">{{ m.name_ko }}</span>{% endif %}
            </h3>

            <p class="ppl-role">
              {{ m.role }}{% if m.joined %}<span class="ppl-joined"> · Joined {{ m.joined }}</span>{% endif %}
            </p>

            {% if m.topic %}
              <p class="ppl-topic">
                <span class="ppl-topic-label">Research Focus</span>
                {{ m.topic }}
              </p>
            {% endif %}
          </div>
        </article>
      {% endfor %}
    </div>
  </section>
{% endif %}

{% if undergrads and undergrads != empty %}
  <section aria-labelledby="ppl-undergraduate-heading">
    <h2 class="ppl-head ppl-anchor" id="ppl-undergraduate-heading">
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
              width="600"
              height="750"
              style="object-position: {{ m.photo_position | default: 'center 25%' }};"
            >
          {% else %}
            <div class="ppl-photo-blank" aria-hidden="true">
              {% if m.initials %}{{ m.initials }}{% else %}{{ m.name_en | slice: 0, 1 }}{% endif %}
            </div>
          {% endif %}

          <div class="ppl-member-copy">
            <h3 class="ppl-name">
              {{ m.name_en }}{% if m.name_ko %}<span class="ppl-name-ko" lang="ko">{{ m.name_ko }}</span>{% endif %}
            </h3>

            <p class="ppl-role">
              {{ m.role }}{% if m.joined %}<span class="ppl-joined"> · Joined {{ m.joined }}</span>{% endif %}
            </p>

            {% if m.topic %}
              <p class="ppl-topic">
                <span class="ppl-topic-label">Research Involvement</span>
                {{ m.topic }}
              </p>
            {% endif %}
          </div>
        </article>
      {% endfor %}
    </div>
  </section>
{% endif %}

{% if shared_contact %}
  <aside class="ppl-shared-contact ppl-anchor" id="ppl-workspace" aria-label="Student workspace and shared telephone">
    <div class="ppl-shared-contact-item">
      <span class="ppl-shared-contact-label">
        Student Workspace
        <span class="ppl-shared-contact-ko" lang="ko">학생 연구공간</span>
      </span>
      <p class="ppl-shared-contact-value">
        {{ shared_contact.room_en }}<br>
        <span lang="ko">{{ shared_contact.room_ko }}</span>
      </p>
    </div>

    <div class="ppl-shared-contact-item">
      <span class="ppl-shared-contact-label">
        Shared Phone
        <span class="ppl-shared-contact-ko" lang="ko">공용 전화</span>
      </span>
      <p class="ppl-shared-contact-value">
        <a href="tel:{{ shared_contact.phone_href }}">{{ shared_contact.phone }}</a>
      </p>
    </div>
  </aside>
{% endif %}

{% if alumni and alumni != empty %}
  <section aria-labelledby="ppl-alumni-heading">
    <h2 class="ppl-head ppl-anchor" id="ppl-alumni-heading">
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
  </section>
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
