---
layout: page
title: People
permalink: /people/
description: Members of the BioMolE Lab at Chungnam National University.
nav: true
nav_order: 4
---

<style>
  /* Top-level section headings: consistent with the rest of the website */
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
    font-weight: 600;
    text-decoration: none;
  }

  .ppl-pi-links a:hover,
  .ppl-pi-links a:focus-visible {
    text-decoration: underline;
    text-underline-offset: 4px;
  }

  /* Education and appointments: visually nested under the PI section */
  .ppl-cv-under-pi {
    margin: 2.2rem 0 1rem;
    padding-top: 1.45rem;
    border-top: 1px solid var(--global-divider-color, #e0e0e0);
  }

  .ppl-cv {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 2.4rem 2.8rem;
    align-items: start;
    margin: 0;
  }

  .ppl-cv h3 {
    margin: 0 0 1.05rem;
    padding-bottom: 0.5rem;
    border-bottom: 1px solid var(--global-divider-color, #e0e0e0);
    color: var(--joinus-accent, #1a3a6b);
    font-size: 1rem;
    font-weight: 700;
    line-height: 1.4;
  }

  .ppl-cv-ko {
    margin-left: 0.45rem;
    color: var(--global-text-color-light);
    font-size: 0.83rem;
    font-weight: 400;
  }

  .ppl-cv ul {
    margin: 0;
    padding: 0;
    list-style: none;
  }

  .ppl-cv li {
    margin-bottom: 1.1rem;
  }

  .ppl-cv li:last-child {
    margin-bottom: 0;
  }

  .ppl-cv-when {
    display: block;
    margin-bottom: 0.1rem;
    color: var(--global-text-color-light);
    font-size: 0.79rem;
    font-variant-numeric: tabular-nums;
    letter-spacing: 0.02em;
  }

  .ppl-cv-what {
    display: block;
    font-size: 0.9rem;
    font-weight: 600;
    line-height: 1.45;
  }

  .ppl-cv-where {
    display: block;
    margin-top: 0.08rem;
    color: var(--global-text-color-light);
    font-size: 0.84rem;
    line-height: 1.5;
  }

  /* Student profiles: generous two-column layout on desktop */
  .ppl-grid {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 2.9rem 2.4rem;
    margin: 2.25rem 0 1.2rem;
  }

  .ppl-member {
    display: grid;
    grid-template-columns: 165px minmax(0, 1fr);
    gap: 1.25rem;
    align-items: start;
    min-width: 0;
    padding-bottom: 1.7rem;
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
    padding-top: 0.05rem;
  }

  .ppl-member-no-topic .ppl-member-copy {
    align-self: center;
  }

  .ppl-name {
    margin: 0 0 0.28rem;
    color: var(--joinus-accent, #1a3a6b);
    font-size: 1.08rem;
    font-weight: 700;
    line-height: 1.4;
  }

  .ppl-role {
    margin: 0;
    color: var(--global-text-color-light);
    font-size: 0.86rem;
    line-height: 1.55;
  }

  .ppl-email {
    margin: 0.38rem 0 0;
    font-size: 0.82rem;
    line-height: 1.5;
    overflow-wrap: anywhere;
  }

  .ppl-email a,
  .ppl-email a:visited {
    color: var(--global-theme-color, #1a4d3e);
    font-weight: 500;
    text-decoration: none;
  }

  .ppl-email a:hover,
  .ppl-email a:focus-visible {
    text-decoration: underline;
    text-underline-offset: 3px;
  }

  .ppl-joined {
    white-space: nowrap;
  }

  .ppl-topic {
    margin: 0.95rem 0 0;
    font-size: 0.9rem;
    line-height: 1.65;
  }

  .ppl-topic-label {
    display: block;
    margin-bottom: 0.24rem;
    color: var(--global-theme-color, #1a4d3e);
    font-size: 0.7rem;
    font-weight: 700;
    letter-spacing: 0.065em;
    line-height: 1.35;
    text-transform: uppercase;
  }

  /* Shared student office and lab contact: simple ruled layout */
  .ppl-shared-contact {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 1.2rem 2.8rem;
    margin: 3.1rem 0 0.8rem;
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
    line-height: 1.4;
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
    line-height: 1.6;
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

  /* Join Us: simple ruled layout, without a card or boxed button */
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
      grid-template-columns: 1fr;
      gap: 2.25rem;
    }

    .ppl-member {
      grid-template-columns: 175px minmax(0, 1fr);
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

    .ppl-cv {
      grid-template-columns: 1fr;
      gap: 2.1rem;
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
      margin-top: 0.75rem;
      font-size: 0.86rem;
    }
  }

  @media (max-width: 420px) {
    .ppl-grid {
      gap: 2.1rem;
    }

    .ppl-member {
      grid-template-columns: 1fr;
      gap: 0.95rem;
      padding-bottom: 1.8rem;
    }

    .ppl-photo,
    .ppl-photo-blank {
      width: min(220px, 72vw);
    }

    .ppl-member-no-topic .ppl-member-copy {
      align-self: start;
    }
  }
</style>

<section aria-labelledby="ppl-pi-heading">
  <h2 class="ppl-head ppl-head-first" id="ppl-pi-heading">
    Principal Investigator
    <span class="ppl-head-ko" lang="ko">연구책임자</span>
  </h2>

  <div class="ppl-pi">
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
        Prof. Choi investigates how molecular interactions govern biomolecular
        organization and how these principles can be translated into functional
        biomaterials, biocatalysis, and bioprocesses. His research integrates
        protein engineering, quantitative biophysics, synthetic biology, and
        bioprocess engineering.
      </p>

      <nav class="ppl-pi-links" aria-label="Principal investigator links">
        <a href="{{ '/research/' | relative_url }}">Research</a>
        <a href="{{ '/publications/' | relative_url }}">Publications</a>
        <a href="{{ '/contact/' | relative_url }}">Contact</a>
      </nav>
    </div>
  </div>

  {% assign cv_sections = site.data.pi_cv.sections %}
  {% if cv_sections and cv_sections != empty %}
    <div class="ppl-cv-under-pi" aria-label="Education and academic appointments">
      <div class="ppl-cv">
        {% for sec in cv_sections %}
          <section>
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
    </div>
  {% endif %}
</section>

{% assign grads = site.data.members.graduate %}
{% if grads and grads != empty %}
  <section aria-labelledby="ppl-graduate-heading">
    <h2 class="ppl-head" id="ppl-graduate-heading">
      Graduate Students
      <span class="ppl-head-ko" lang="ko">대학원생</span>
    </h2>

    <div class="ppl-grid">
      {% for m in grads %}
        <article class="ppl-member{% unless m.topic %} ppl-member-no-topic{% endunless %}">
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

            {% if m.email %}
              <p class="ppl-email">
                <a href="mailto:{{ m.email }}">{{ m.email }}</a>
              </p>
            {% endif %}

            {% if m.topic %}
              <p class="ppl-topic">
                <span class="ppl-topic-label">Research focus</span>
                {{ m.topic }}
              </p>
            {% endif %}
          </div>
        </article>
      {% endfor %}
    </div>
  </section>
{% endif %}

{% assign undergrads = site.data.members.undergraduate %}
{% if undergrads and undergrads != empty %}
  <section aria-labelledby="ppl-undergraduate-heading">
    <h2 class="ppl-head" id="ppl-undergraduate-heading">
      Undergraduate Researchers
      <span class="ppl-head-ko" lang="ko">학부연구생</span>
    </h2>

    <div class="ppl-grid">
      {% for m in undergrads %}
        <article class="ppl-member{% unless m.topic %} ppl-member-no-topic{% endunless %}">
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

            {% if m.email %}
              <p class="ppl-email">
                <a href="mailto:{{ m.email }}">{{ m.email }}</a>
              </p>
            {% endif %}

            {% if m.topic %}
              <p class="ppl-topic">
                <span class="ppl-topic-label">Research focus</span>
                {{ m.topic }}
              </p>
            {% endif %}
          </div>
        </article>
      {% endfor %}
    </div>
  </section>
{% endif %}

{% assign shared_contact = site.data.members.shared_contact %}
{% if shared_contact %}
  <aside class="ppl-shared-contact" aria-label="Student office and shared lab contact">
    <div class="ppl-shared-contact-item">
      <span class="ppl-shared-contact-label">
        Student Office
        <span class="ppl-shared-contact-ko" lang="ko">학생 연구공간</span>
      </span>
      <p class="ppl-shared-contact-value">
        {{ shared_contact.room_en }}<br>
        <span lang="ko">{{ shared_contact.room_ko }}</span>
      </p>
    </div>

    <div class="ppl-shared-contact-item">
      <span class="ppl-shared-contact-label">
        Shared Lab Phone
        <span class="ppl-shared-contact-ko" lang="ko">공용 전화</span>
      </span>
      <p class="ppl-shared-contact-value">
        <a href="tel:{{ shared_contact.phone_href }}">{{ shared_contact.phone }}</a>
      </p>
    </div>
  </aside>
{% endif %}

{% assign alumni = site.data.members.alumni %}
{% if alumni and alumni != empty %}
  <section aria-labelledby="ppl-alumni-heading">
    <h2 class="ppl-head" id="ppl-alumni-heading">
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

