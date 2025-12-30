---
layout: default
title: "Home"
permalink: /
description: "Portfolio of Siddharth Dongre - wireless security, adversarial modeling, and secure coexistence."
---

<div class="grid">
  <aside class="headshot">
    <img class="headshot__img"
       src="{{ '/assets/img/SDongre.jpg' | relative_url }}"
       alt="Siddharth Dongre headshot">
  </aside>

  <section>
    <p> I am a security researcher specializing in wireless communications and cybersecurity. My work is focused on developing fair, robust and secure spectrum sharing techniques for 5G networks as they coexist with competing protocols, such as Wi-Fi, and incumbent services, such as radio astronomy systems. My lightweight solutions facilitate concurrent operation of coexisting wireless systems while limiting unintended interference and mitigating adversarial attacks. My work has been published in multiple peer-reviewed venues including the top-ranked IEEE Transactions on Information Forensics and Security. I am currently working towards developing interoperable protocol-agnostic coexistence frameworks for seamless and secure wireless coexistence with both terrestrial and non-terrestrial communication systems.</p>
  </section>
</div>

<hr/>

<section class="card">
  <h2 class="h2" style="margin-top:0;">Research Interests</h2>
  <ul>
    <li><strong>Spectrum sharing fairness in adversarial scenarios:</strong> modelling attacks and defenses for in unlicensed/shared bands.</li>
    <li><strong>Secure 5G and Wi-Fi Coexistence:</strong> coordination mechanisms that prevent starvation attacks and improve robustness.</li>
    <li><strong>Coexistence with incumbents:</strong> low-latency interference nulling and resilient beamforming for coexistence with radio astronomy.</li>
    <li><strong>Vehicular Networks (NR-V2X):</strong> adaptive numerology for reliable delivery of safety messages in dense, high-mobility settings.</li>
    <li><strong>System validation:</strong> SDR testbeds, reproducible experiments, and measurable security/performance trade-offs.</li>
  </ul>
</section>

<h2 class="h2">Selected Publications</h2>

{% assign featured = site.publications | where: "featured", true | sort: "year" | reverse %}
{% for p in featured limit:3 %}
  {% include pub_item.html citation=p.citation pdf=p.pdf doi=p.doi %}
{% endfor %}

<p><a href="{{ '/publications/' | relative_url }}">View all publications →</a></p>
