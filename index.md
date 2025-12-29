---
layout: default
title: "Home"
permalink: /
description: "Portfolio of Siddharth Dongre - wireless security, adversarial modeling, and secure coexistence."
---

<div class="grid">
  <aside class="headshot">
    <div class="headshot__box">
      Headshot placeholder<br/>
      <span style="font-size:0.9rem;">Replace later with your photo (3:4 portrait).</span>
    </div>
  </aside>

  <section>
    <h1 class="h1">Bio</h1>
    <p>I am a Ph.D. candidate in Electrical and Computer Engineering at the Rochester Institute of Technology (RIT), where I study wireless security and secure communications with an emphasis on adversarial modeling in shared-spectrum systems. My research develops fair, robust, and attack-resilient coexistence mechanisms that allow 5G networks to operate harmoniously alongside competing protocols such as Wi-Fi and alongside incumbents such as radio astronomy services. I combine theory-driven design (threat modeling, robust optimization, and signal processing) with practical validation using software-defined radio (SDR) testbeds to ensure deployability under real-world constraints such as latency, limited feedback, and strategic/adaptive attackers.</p><p>My long-term goal is to build universal coexistence methods for heterogeneous wireless environments where security, reliability, and spectrum efficiency must be achieved simultaneously. In teaching, I aim to help students reason from threat models to implementations: how protocol choices create vulnerabilities, how adversaries exploit them, and how defensible system designs can be validated experimentally. My work has appeared in peer-reviewed venues including IEEE Transactions on Information Forensics and Security and IEEE Transactions on Cognitive Communications and Networking, and I have served as an adjunct instructor for Introduction to Cybersecurity with consistently strong student feedback.</p>

    <div class="badges" aria-label="Research themes">
      <span class="badge">Adversarial modeling in shared spectrum</span>
      <span class="badge">Wireless security & secure communications</span>
      <span class="badge">5G ↔ Wi-Fi coexistence</span>
      <span class="badge">Incumbent protection (radio astronomy)</span>
      <span class="badge">SDR prototyping & experimentation</span>
    </div>
  </section>
</div>

<hr/>

<section class="card">
  <h2 class="h2" style="margin-top:0;">Research Interests (at a glance)</h2>
  <ul>
    <li><strong>Adversarial coexistence and spectrum fairness:</strong> threat models and defenses for strategic attackers in unlicensed/shared bands.</li>
    <li><strong>Secure 5G NR-U / Wi-Fi interaction:</strong> coordination mechanisms that prevent starvation and improve robustness.</li>
    <li><strong>Incumbent-aware 5G security:</strong> low-latency interference nulling and resilient beamforming for coexistence with radio astronomy.</li>
    <li><strong>Vehicular wireless security (NR-V2X):</strong> adaptive numerology and reliable delivery of safety messages in dense, high-mobility settings.</li>
    <li><strong>System validation:</strong> SDR testbeds, reproducible experiments, and measurable security/performance trade-offs.</li>
  </ul>
</section>

<h2 class="h2">Selected Publications</h2>
<p class="lead">Edit which items appear here by toggling <code>featured: true</code> inside the corresponding file in <code>_publications/</code>.</p>

{% assign featured = site.publications | where: "featured", true | sort: "year" | reverse %}
{% for p in featured limit:3 %}
  {% include pub_item.html citation=p.citation pdf=p.pdf doi=p.doi %}
{% endfor %}

<p><a href="{{ '/publications/' | relative_url }}">View all publications →</a></p>
