---
layout: page
title: News & Awards
permalink: /news/
nav: true
nav_order: 5
---

<style>
  /*
   * Page introduction
   */
  .news-page-lead {
    max-width: 700px;
    margin: -0.2rem 0 2.4rem;
    color: var(--global-text-color-light);
    font-size: 1.02rem;
    line-height: 1.65;
  }

  /*
   * Featured notice
   */
  .featured-notice {
  display: grid;
  grid-template-columns: minmax(280px, 330px) minmax(0, 1fr);
  align-items: center;
  gap: clamp(1.4rem, 2.5vw, 2rem);
  max-width: 920px;
  box-sizing: border-box;
  margin: 0 auto 3.8rem;
  padding: clamp(1.3rem, 2.8vw, 2rem);
  border: 1px solid var(--global-divider-color, #dfe3e8);
  border-radius: 14px;
  background: var(--global-card-bg-color, var(--global-bg-color, #ffffff));
  box-shadow: 0 12px 30px rgba(0, 0, 0, 0.06);
}
  
  .notice-poster {
    display: block;
    width: 100%;
    overflow: hidden;
    border: 1px solid var(--global-divider-color, #dfe3e8);
    border-radius: 10px;
    background: #ffffff;
    box-shadow: 0 8px 20px rgba(0, 0, 0, 0.09);
    transition:
      transform 0.18s ease,
      box-shadow 0.18s ease;
  }

  .notice-poster:hover,
  .notice-poster:focus-visible {
    box-shadow: 0 12px 26px rgba(0, 0, 0, 0.13);
    transform: translateY(-3px);
  }

  .notice-poster:focus-visible {
    outline: 3px solid rgba(26, 77, 62, 0.25);
    outline-offset: 3px;
  }

  .notice-poster img {
    display: block;
    width: 100%;
    height: auto;
  }

  .notice-content {
    min-width: 0;
  }

  .notice-label {
    display: inline-flex;
    align-items: center;
    margin-bottom: 0.85rem;
    padding: 0.3rem 0.68rem;
    border: 1px solid var(--joinus-accent, #1a3a6b);
    border-radius: 999px;
    color: var(--joinus-accent, #1a3a6b);
    font-size: 0.7rem;
    font-weight: 800;
    letter-spacing: 0.09em;
    line-height: 1.2;
  }

  .notice-organization {
    margin: 0 0 0.55rem;
    color: var(--global-text-color-light);
    font-size: 1.08rem;
    font-weight: 600;
    line-height: 1.6;
  }

  .notice-title {
    margin: 0 0 0.2rem;
    color: var(--joinus-accent, #1a3a6b);
    font-size: clamp(1.25rem, 2.2vw, 1.6rem);
    font-weight: 700;
    line-height: 1.42;
  }

  .notice-summary {
    margin: 0.8rem 0 1.25rem;
    color: var(--global-text-color-light);
    font-size: 0.94rem;
    line-height: 1.65;
  }

  .notice-actions {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    gap: 0.75rem 1.1rem;
    margin-top: 1.5rem;
  }

  .notice-button,
  .notice-button:visited {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    min-height: 42px;
    box-sizing: border-box;
    padding: 0.68rem 1rem;
    border: 2px solid var(--joinus-accent, #1a3a6b);
    border-radius: 999px;
    background: var(--joinus-accent, #1a3a6b);
    color: #ffffff;
    font-size: 0.86rem;
    font-weight: 700;
    line-height: 1.2;
    text-decoration: none;
    white-space: nowrap;
    transition:
      transform 0.18s ease,
      box-shadow 0.18s ease;
  }

  .notice-button:hover,
  .notice-button:focus-visible {
    box-shadow: 0 8px 18px rgba(0, 0, 0, 0.14);
    color: #ffffff;
    text-decoration: none;
    transform: translateY(-2px);
  }

  .notice-button:focus-visible {
    outline: 3px solid rgba(26, 77, 62, 0.25);
    outline-offset: 3px;
  }

  .notice-secondary-link,
  .notice-secondary-link:visited {
    color: var(--global-theme-color, #145a46);
    font-size: 0.88rem;
    font-weight: 700;
    line-height: 1.4;
    text-decoration: none;
    white-space: nowrap;
  }

  .notice-secondary-link:hover,
  .notice-secondary-link:focus-visible {
    text-decoration: underline;
    text-underline-offset: 4px;
  }

  /*
   * Latest news heading
   */
  .latest-news-header {
    margin-bottom: 1.15rem;
  }

  .latest-news-title {
    margin: 0;
    color: var(--joinus-accent, #1a3a6b);
    font-size: 1.55rem;
    font-weight: 700;
    line-height: 1.25;
  }

  .latest-news-subtitle {
    margin: 0.35rem 0 0;
    color: var(--global-text-color-light);
    font-size: 0.94rem;
    line-height: 1.5;
  }

  /*
   * News list
   */
  .news-feed {
    border-top: 1px solid var(--global-divider-color, #dfe3e8);
  }

  .news-item {
    display: grid;
    grid-template-columns: 112px minmax(0, 1fr);
    gap: 1.35rem;
    align-items: start;
    padding: 1.15rem 0.15rem;
    border-bottom: 1px solid var(--global-divider-color, #dfe3e8);
  }

  .news-item-date {
    padding-top: 0.08rem;
    color: var(--global-text-color-light);
    font-size: 0.82rem;
    font-weight: 500;
    font-variant-numeric: tabular-nums;
    letter-spacing: 0.025em;
    line-height: 1.55;
    white-space: nowrap;
  }

  .news-item-main {
    min-width: 0;
  }

  /*
   * category가 있는 뉴스에만 표시됩니다.
   */
  .news-item-category {
    display: inline-flex;
    margin: 0 0 0.4rem;
    padding: 0.18rem 0.52rem;
    border: 1px solid var(--global-divider-color, #dfe3e8);
    border-radius: 999px;
    color: var(--global-text-color-light);
    font-size: 0.69rem;
    font-weight: 700;
    letter-spacing: 0.035em;
    line-height: 1.3;
  }

  .news-item-title {
    color: var(--global-text-color);
    font-size: 0.98rem;
    font-weight: 600;
    line-height: 1.58;
  }

  a.news-item-title,
  a.news-item-title:visited {
    color: var(--global-text-color);
    text-decoration: none;
  }

  a.news-item-title::after {
    display: inline-block;
    margin-left: 0.4rem;
    color: var(--global-theme-color, #145a46);
    content: "→";
    opacity: 0;
    transform: translateX(-4px);
    transition:
      opacity 0.18s ease,
      transform 0.18s ease;
  }

  a.news-item-title:hover,
  a.news-item-title:focus-visible {
    color: var(--global-theme-color, #145a46);
    text-decoration: underline;
    text-decoration-thickness: 1px;
    text-underline-offset: 4px;
  }

  a.news-item-title:hover::after,
  a.news-item-title:focus-visible::after {
    opacity: 1;
    transform: translateX(0);
  }

  .news-empty {
    margin: 1.5rem 0;
    color: var(--global-text-color-light);
  }

  /*
   * Tablet and mobile
   */
  @media (max-width: 720px) {
    .featured-notice {
      grid-template-columns: 1fr;
      max-width: 560px;
    }

    .notice-poster {
      width: 100%;
      max-width: 245px;
      justify-self: center;
    }

    .notice-content {
      text-align: center;
    }

    .notice-actions {
      justify-content: center;
    }

    .news-item {
      grid-template-columns: 1fr;
      gap: 0.25rem;
      padding: 1rem 0;
    }

    .news-item-date {
      font-size: 0.78rem;
    }
  }

  @media (max-width: 480px) {
    .featured-notice {
      padding: 1.2rem;
      border-radius: 12px;
    }

    .notice-actions {
      flex-direction: column;
      align-items: stretch;
    }

    .notice-button,
    .notice-secondary-link {
      width: 100%;
      box-sizing: border-box;
      justify-content: center;
      text-align: center;
    }
  }

  @media (prefers-reduced-motion: reduce) {
    .notice-poster,
    .notice-button,
    a.news-item-title::after {
      transition: none;
    }
  }
</style>

<p class="news-page-lead">
  Research updates, publications, awards, and opportunities from the BioMolE Lab.
</p>

<section class="featured-notice" aria-labelledby="featured-notice-title">
  <a
    class="notice-poster"
    href="{{ '/assets/img/notice_synbridge.jpg' | relative_url }}"
    target="_blank"
    rel="noopener noreferrer"
    aria-label="대학원생 모집 포스터 크게 보기"
  >
    <img
      src="{{ '/assets/img/notice_synbridge.jpg' | relative_url }}"
      alt="충남대학교 합성생물공학전공 대학원생 모집 포스터"
    >
  </a>

  <div class="notice-content">
  <p class="notice-organization" lang="ko">
    충남대학교 공과대학 응용화학공학과 합성생물공학전공
  </p>

  <h2 class="notice-title" id="featured-notice-title" lang="ko">
    미래 바이오 산업 혁신의 중심에서 성장할<br>
    열정 있는 대학원생을 모집합니다.
  </h2>
</div>
</section>

<section aria-labelledby="latest-news-title">
  <header class="latest-news-header">
    <h2 class="latest-news-title" id="latest-news-title">
      Latest News
    </h2>

    <p class="latest-news-subtitle" lang="ko">
      연구실의 최근 연구성과와 수상 소식입니다.
    </p>
  </header>

  {% if site.news != blank %}
    {% assign news_items = site.news | reverse %}

    <div class="news-feed">
      {% for item in news_items %}
        <article class="news-item">
          <time
            class="news-item-date"
            datetime="{{ item.date | date_to_xmlschema }}"
          >
            {{ item.date | date: '%Y.%m.%d' }}
          </time>

          <div class="news-item-main">
            {% if item.category %}
              <div class="news-item-category">
                {{ item.category }}
              </div>
            {% endif %}

            {% if item.inline %}
              <div class="news-item-title">
                {{ item.content | remove: '<p>' | remove: '</p>' | emojify }}
              </div>
            {% else %}
              <a
                class="news-item-title"
                href="{{ item.url | relative_url }}"
              >
                {{ item.title }}
              </a>
            {% endif %}
          </div>
        </article>
      {% endfor %}
    </div>
  {% else %}
    <p class="news-empty">
      No news so far.
    </p>
  {% endif %}
</section>
