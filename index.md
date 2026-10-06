---
layout: page
title: AI Security & AI for Science
last_modified_at: 2026-10-05
---

<section class="hero" id="about" aria-labelledby="about-title">
  <div class="hero-intro">
    <span class="anchor-alias" id="about-me" aria-hidden="true"></span>
    <p class="eyebrow">Northwestern University</p>
    <h1 id="about-title">Nan Yan<span class="name-dot" aria-hidden="true">.</span></h1>
    <p class="hero-role">PhD student in Computer Science</p>
    <ul class="research-topics" id="research-interests" aria-label="Research interests">
      <li>LLM security</li>
      <li>Agent security</li>
      <li>AI4Science</li>
    </ul>
    <ul class="contact-links" aria-label="Contact and academic profiles">
      <li><a class="contact-primary" href="mailto:{{ site.owner.email }}">Email <span aria-hidden="true">&nearr;</span></a></li>
      <li><a href="{{ site.owner.scholar }}">Google Scholar <span aria-hidden="true">&nearr;</span></a></li>
      <li><a href="https://github.com/{{ site.owner.github }}">GitHub <span aria-hidden="true">&nearr;</span></a></li>
      <li><a href="https://www.linkedin.com/in/{{ site.owner.linkedin }}/">LinkedIn <span aria-hidden="true">&nearr;</span></a></li>
    </ul>
    <div class="hero-bio">
      <p>I am a first-year PhD student at Northwestern University, advised by <a href="https://users.cs.northwestern.edu/~ychen/">Prof. Yan Chen</a>. My current research focuses on the <strong>safety and security of recursive self-improvement (RSI) and AI agents</strong>. More recently, I have also begun exploring <strong>AI for Science (AI4Science)</strong>.</p>
      <p>Previously, I received my M.Eng. from Wuhan University, working with <a href="https://liyuqingwhu.github.io/lyq/">Prof. Yuqing Li</a> and <a href="https://cse.whu.edu.cn/info/1101/1784.htm">Prof. Jing Chen</a>, and my B.Eng. from Shandong University.</p>
    </div>
    <p class="hero-contact-note">Always happy to discuss research and collaborations.</p>
  </div>
  <figure class="hero-portrait">
    <picture>
      <source srcset="{{ '/images/photo/portrait.webp' | relative_url }}" type="image/webp">
      <img src="{{ '/images/photo/portrait.jpg' | relative_url }}" alt="Nan Yan outdoors among trees" width="800" height="829" fetchpriority="high">
    </picture>
    <figcaption>Outside research, I enjoy swimming and fitness.</figcaption>
  </figure>
</section>

<section class="content-section news-section" id="news" aria-labelledby="news-title">
  <div class="section-heading">
    <div>
      <p class="eyebrow">Recently</p>
      <h2 id="news-title">News</h2>
    </div>
    <span class="section-aside">Updates &amp; milestones</span>
  </div>
  <ul class="news-list">
    {% for item in site.data.news limit: 4 %}
    <li><time datetime="{{ item.date }}">{{ item.date | append: '-01' | date: '%b %Y' }}</time><div class="news-content"><span class="news-icon" aria-hidden="true">{{ item.icon }}</span><div>{{ item.text | markdownify }}</div></div></li>
    {% endfor %}
  </ul>
  <details class="archive">
    <summary>Earlier updates <span class="archive-count">{{ site.data.news.size | minus: 4 }}</span></summary>
    <ul class="news-list">
      {% for item in site.data.news offset: 4 %}
      <li><time datetime="{{ item.date }}">{{ item.date | append: '-01' | date: '%b %Y' }}</time><div class="news-content"><span class="news-icon" aria-hidden="true">{{ item.icon }}</span><div>{{ item.text | markdownify }}</div></div></li>
      {% endfor %}
    </ul>
  </details>
</section>

<section class="content-section" id="publications" aria-labelledby="publications-title">
  <div class="section-heading">
    <div>
      <p class="eyebrow">Research</p>
      <h2 id="publications-title">Publications</h2>
    </div>
    <a class="section-link" href="{{ site.owner.scholar }}">Google Scholar <span aria-hidden="true">&nearr;</span></a>
  </div>
  <p class="list-label">Selected work</p>
  <ul class="publication-list">
    {% assign selected_papers = site.data.publications | where: 'featured', true %}
    {% for paper in selected_papers %}
      {% include publication.html paper=paper %}
    {% endfor %}
  </ul>
  <p class="list-label more-publications-label">More publications</p>
  <ul class="publication-list">
    {% assign other_papers = site.data.publications | where: 'featured', false %}
    {% for paper in other_papers %}
      {% include publication.html paper=paper %}
    {% endfor %}
  </ul>
</section>

<section class="content-section" id="experience" aria-labelledby="experience-title">
  <span class="anchor-alias" id="experiences" aria-hidden="true"></span>
  <div class="section-heading">
    <div>
      <p class="eyebrow">Along the way</p>
      <h2 id="experience-title">Experience</h2>
    </div>
  </div>
  <div class="experience-grid">
    <article class="experience-card">
      <p class="experience-date"><time datetime="2026-04">Apr 2026</time> &ndash; <time datetime="2026-09">Sep 2026</time></p>
      <h3 class="experience-brand"><img class="experience-logo" src="{{ '/images/logo/microsoft.png' | relative_url }}" alt="Microsoft" width="216" height="46" loading="lazy" decoding="async"></h3>
      <p class="experience-role">Research Intern</p>
      <p>Mentors: Xiaoting Qin and Fangkai Yang</p>
      <p class="experience-project">Agent security, RSI attack</p>
    </article>
    <article class="experience-card">
      <p class="experience-date"><time datetime="2025-06">Jun 2025</time> &ndash; <time datetime="2026-02">Feb 2026</time></p>
      <h3 class="experience-brand"><img class="experience-logo" src="{{ '/images/logo/rice-university.svg' | relative_url }}" alt="Rice University" width="525" height="75" loading="lazy" decoding="async"></h3>
      <p class="experience-role">Research Intern</p>
      <p>Working with <a href="https://jxing.me/">Prof. Jiarong Xing</a></p>
      <p class="experience-project">Agent security, memory attack</p>
    </article>
  </div>
</section>

<section class="content-section honors-section" id="honors" aria-labelledby="honors-title">
  <span class="anchor-alias" id="scholarships-and-honors" aria-hidden="true"></span>
  <div class="section-heading">
    <div>
      <p class="eyebrow">Recognition</p>
      <h2 id="honors-title">Scholarships &amp; honors</h2>
    </div>
  </div>
  <ul class="honors-list">
    <li><span><strong>Cyberspace Security Innovation Grant</strong><span class="honor-detail">TOPSEC '23, Huawei '25 &amp; DiDi '26</span></span><span class="honor-year">2023, 2025, 2026</span></li>
    <li><span><strong>Outstanding Graduate Award</strong><span class="honor-detail">Shandong University '23 &amp; Wuhan University '26</span></span><span class="honor-year">2023, 2026</span></li>
    <li><span><strong>National Scholarship</strong><span class="honor-detail">Top 0.2% nationwide &middot; Ministry of Education, China</span></span><span class="honor-year">2024, 2025</span></li>
    <li><span><strong>BYD Scholarship</strong><span class="honor-detail">Top 3 in the Department of CSE &middot; Wuhan University</span></span><span class="honor-year">2025</span></li>
    <li><span><strong>USENIX Security Student Grant</strong></span><span class="honor-year">2025</span></li>
    <li><span><strong>Merit Student</strong><span class="honor-detail">Top 1% &middot; Wuhan University</span></span><span class="honor-year">2024, 2025</span></li>
    <li><span><strong>First Class Scholarship</strong><span class="honor-detail">Award rate: 5% university-wide &middot; Wuhan University</span></span><span class="honor-year">2024, 2025</span></li>
  </ul>
  <details class="archive">
    <summary>Earlier honors <span class="archive-count">2</span></summary>
    <ul class="honors-list">
      <li><span><strong>Alumni Council Representative</strong><span class="honor-detail">Department of CSE, 6/101 &middot; Shandong University</span></span><span class="honor-year">2023</span></li>
      <li><span><strong>The Power of Role Models Academy Person of the Year</strong><span class="honor-detail">Top 1 in the Department of CSE &middot; Shandong University</span></span><span class="honor-year">2023</span></li>
    </ul>
  </details>
</section>

{% comment %}
Previously hidden material is retained here and is not published.

Additional collaborations: Prof. Bo Li (HKUST), https://www.cse.ust.hk/~bli/,
and Prof. Xiong Wang, https://wangxionghome.github.io/.

Research Intern, Pennsylvania State University, working with Prof. Peng Liu,
https://s2.ist.psu.edu/pliu/, 2025. Project: Static code analysis of agent memory.

Competition Awards
- Third Prize of the 2-nd National Open Source Security Award Program, Cyber Security Association, China (2026)
- Second Prize of the 1-st National Open Source Security Award Program, Cyber Security Association, China (2025)
- Second Prize of The 7-th National College Cryptography Mathematics Contest, Chinese Association for Cryptologic Research, China (2022)
- Second Prize of The 15-th National College Student Information Security Competition, Cyber Security Association, China (2022)
- First Prize of The 7-th National College Cryptography Mathematics Contest, Chinese Association for Cryptologic Research, North China Division (2022)
- First Prize of The 31-th China Undergraduate Mathematical Contest in Modeling, Shandong Province (2021)

Patents and Software Copyrights
- "Differential privacy-based heterogeneous federal fine tuning language model construction method and system", China Patent Application ZL 2024 1 1379992.3, PatentGrant (Sep 2025)
- "Large language model training method and system based on elastic federated low-rank adaptive fine-tuning", China Patent Application CN119443311A, PatentPending (Feb 2025)
- "Method for constructing a vertical federated learning system based on participant selection and parameter freezing", China Patent Application CN202411465068.7, PatentPending (Jan 2025)
- "Cross-silo heterogeneous federated learning system based on homomorphic encryption V1.0", China Software Copyrights 2024SR1516588 (Oct 2024)
- "Method and device for constructing cross-silo heterogeneous federated learning system based on homomorphic encryption", China Patent Application CN117892322A, PatentPending (Apr 2024)
- "Network traffic obfuscation method, device, equipment and medium", China Patent Application CN117749402A, PatentPending (Mar 2024)

Disabled visitor map: https://clustrmaps.com/site/1c589
https://www.clustrmaps.com/map_v2.png?d=SyeUVfbLgTPj_Jd0Sk1e10UKgOSeqim_lijx_SJdDeA&cl=ffffff&t=tt
{% endcomment %}
