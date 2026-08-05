---
permalink: /
title: false
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<style>
.news-rail{
  --accent: var(--global-base-color, #2f7f93);
  --ink: var(--global-text-color, #4b5158);
  float: right;
  width: 310px;
  max-width: 100%;
  margin: .2rem 0 1.4rem 1.9rem;
  padding: 1rem 1.1rem .9rem;
  border-radius: 14px;
  background: var(--global-card-bg-color, #fff);
  border: 1px solid color-mix(in srgb, var(--accent) 20%, transparent);
  box-shadow: 0 1px 2px rgba(16,24,32,.04),
              0 12px 28px -14px color-mix(in srgb, var(--accent) 30%, transparent);
}
.news-rail__title{
  font-family: "IBM Plex Mono", ui-monospace, monospace;
  font-size: .72rem;
  letter-spacing: .28em;
  text-transform: uppercase;
  color: var(--accent);
  margin: 0 0 .75rem;
  padding: 0;
  border: 0;
}
/* The list scrolls; the card itself stays put. */
.news-rail__list{
  list-style: none;
  margin: 0;
  padding: 0 .5rem 0 0;
  max-height: 340px;
  overflow-y: auto;
  overscroll-behavior: contain;
}
.news-rail__list > li{
  position: relative;
  padding: 0 0 .8rem 1.1rem;
  margin: 0 0 .8rem;
  border-bottom: 1px solid color-mix(in srgb, var(--accent) 14%, transparent);
  font-size: .87rem;
  line-height: 1.5;
  color: var(--ink);
}
.news-rail__list > li:last-child{
  border-bottom: 0;
  margin-bottom: 0;
  padding-bottom: 0;
}
.news-rail__list > li::before{
  content: "";
  position: absolute;
  left: 0;
  top: .58em;
  width: .38rem;
  height: .38rem;
  border-radius: 50%;
  background: var(--accent);
}
.news-rail__date{
  display: block;
  margin-top: .2rem;
  font-family: "IBM Plex Mono", ui-monospace, monospace;
  font-size: .72rem;
  letter-spacing: .04em;
  color: color-mix(in srgb, var(--ink) 60%, transparent);
}
/* Slim scrollbar so the rail reads as a panel, not a textarea. */
.news-rail__list{ scrollbar-width: thin; scrollbar-color: color-mix(in srgb, var(--accent) 45%, transparent) transparent; }
.news-rail__list::-webkit-scrollbar{ width: 6px; }
.news-rail__list::-webkit-scrollbar-track{ background: transparent; }
.news-rail__list::-webkit-scrollbar-thumb{
  background: color-mix(in srgb, var(--accent) 35%, transparent);
  border-radius: 3px;
}
.news-rail__list::-webkit-scrollbar-thumb:hover{
  background: color-mix(in srgb, var(--accent) 55%, transparent);
}
/* Below tablet the rail stops floating and becomes a full-width band. */
@media (max-width: 900px){
  .news-rail{
    float: none;
    width: 100%;
    margin: 0 0 1.5rem;
  }
  .news-rail__list{ max-height: 260px; }
}
</style>

<aside class="news-rail" aria-labelledby="news-rail-title">
  <h2 class="news-rail__title" id="news-rail-title">ScAI Lab News</h2>
  <ul class="news-rail__list">
    <li>ScAI Lab to host 1st Symposium on <strong>Parsimonious SciML</strong> at AAAI 2026 Fall Symposium Series. <a href="https://sites.google.com/view/parsciml-fss26/call-for-participation" target="_blank" rel="noopener noreferrer">website</a><span class="news-rail__date">November 2026</span></li>
    <li>LIGO-PINN framework to overcome PINN catastrophic failures pre-print published. <a href="https://arxiv.org/abs/2607.14233" target="_blank" rel="noopener noreferrer">paper link</a><span class="news-rail__date">July 2026</span></li>
    <li>TRIE: Neural Surrogate Evaluation Framework pre-print published. <a href="https://arxiv.org/abs/2607.00196" target="_blank" rel="noopener noreferrer">paper link</a><span class="news-rail__date">June 2026</span></li>
    <li>Bharat is off for a summer internship at Los-Alamos National Labs.<span class="news-rail__date">Summer 2026</span></li>
    <li>ScAI Lab awarded eBay grant to explore LLM-Modulo search ranking.<span class="news-rail__date">January 2026</span></li>
    <li>Arya admitted to Georgia Tech UG in Fall 2027. Congrats Arya!<span class="news-rail__date">January 2026</span></li>
  </ul>
</aside>

Our group develops machine learning and AI methods that accelerate scientific discovery in domains governed by physical laws, from fluid dynamics and chemistry to the earth sciences. Much of our work centers on **Parsimonious SciML**: <u>designing neural surrogates that faithfully model complex physical systems even under severe data paucity, where simulations are too costly to produce the data that conventional models demand.</u> We are especially motivated by the opportunities modern AI and machine learning offers in accelerating large-scale computational simulations and strive to develop generalizable AI/ML models by embedding scientific domain knowledge directly into models so that predictions remain accurate, physically consistent, and able to generalize beyond the training regime. Our research is supported by organizations like eBay Inc. and Stevens Institute of Technology.

Research Focus
======
<!--
Our group at ScAI lab, is especially focused on leveraging scientific domain knowledge to improve model generalization, decision interpretability and reduce the negative effects of data paucity and noise. Most recently, we have been focused on leveraging machine learning techniques to address challenges in physics (specifically computational fluid dynamics) to alleviate the cost of expensive simulations using science-guided machine learning models.

Our other areas of research interest include:

- Transfer Learning & Domain Adaptation
- Multi-task & Meta Learning
- Time-series Forecasting & Anomaly Detection (especially in the context of Cyber-Physical Systems)
- Intelligent Disaster Management
- Disease Modeling (COVID-19, Influenza-Like-illnesses)
-->

Our work is organized around three interconnected research thrusts. Select a theme below to explore its core challenges and the peer-reviewed publications that address them.

<style>
.focus-grid{
  display: flex;
  flex-direction: column;
  gap: 1.15rem;
  margin: 1.5rem 0 2.5rem;
  width: 100%;
  clear: both; /* never slide under the floated news rail */
}
.focus-card{
  border: 1px solid var(--global-border-color, #e3e8ea);
  border-radius: 14px;
  background: var(--global-card-bg-color, #fff);
  overflow: hidden;
  transition: box-shadow .25s ease, transform .25s ease, border-color .25s ease;
}
.focus-card[open]{
  box-shadow: 0 18px 40px -22px rgba(15,40,55,.5);
  border-color: var(--global-link-color, #52adc8);
}
.focus-card:hover{
  transform: translateY(-2px);
  box-shadow: 0 14px 30px -20px rgba(15,40,55,.45);
}
.focus-card[open]:hover{ transform: none; }
.focus-summary{
  cursor: pointer;
  list-style: none;
  padding: 1.15rem 1.15rem;
  display: block;
  color: var(--global-text-color);
  border-left: 4px solid var(--global-link-color, #52adc8);
  background: linear-gradient(0deg, rgba(82,173,200,.04), rgba(82,173,200,.08));
  transition: background .2s ease;
}
.focus-summary:hover{ background: linear-gradient(0deg, rgba(82,173,200,.08), rgba(82,173,200,.14)); }
.focus-summary::-webkit-details-marker{ display: none; }
.focus-head-row{
  display: flex;
  align-items: center;
  gap: .7rem;
  font-weight: 600;
  font-size: 1.02rem;
  line-height: 1.25;
}
.focus-blurb{
  display: block;
  margin: .6rem 0 0;
  padding-left: calc(34px + .7rem);
  font-weight: 400;
  font-size: .88rem;
  line-height: 1.55;
  color: var(--global-text-color);
}
.focus-hint{
  display: block;
  margin: .5rem 0 0;
  padding-left: calc(34px + .7rem);
  font-size: .74rem;
  font-weight: 600;
  letter-spacing: .03em;
  color: var(--global-link-color, #52adc8);
}
.focus-card[open] .focus-hint .focus-hint-more{ display: none; }
.focus-hint .focus-hint-less{ display: none; }
.focus-card[open] .focus-hint .focus-hint-less{ display: inline; }
@media (max-width: 520px){
  .focus-blurb, .focus-hint{ padding-left: 0; }
}
.focus-icon{
  flex: 0 0 auto;
  width: 34px; height: 34px;
  border-radius: 9px;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  background: var(--global-link-color, #52adc8);
  color: #fff;
  font-size: 1.05rem;
}
/* Line-art icons sit on the same accent tile as the emoji ones. */
.focus-icon svg{
  display: block;
  width: 21px;
  height: 21px;
  fill: none;
  stroke: currentColor;
  stroke-width: 1.4;
  stroke-linecap: round;
  stroke-linejoin: round;
}
.focus-title{ flex: 1 1 auto; }
.focus-chevron{
  flex: 0 0 auto;
  color: var(--global-link-color, #52adc8);
  font-size: .95rem;
  transition: transform .25s ease;
}
.focus-card[open] .focus-chevron{ transform: rotate(180deg); }
.focus-body{
  padding: .3rem 1.25rem 1.35rem;
  animation: focus-fade .3s ease;
  width: 100%;
}
@keyframes focus-fade{ from{ opacity: 0; transform: translateY(-4px);} to{ opacity: 1; transform: none;} }
.focus-section-label{
  display: inline-block;
  margin: 1.1rem 0 .5rem;
  font-size: .72rem;
  font-weight: 700;
  letter-spacing: .09em;
  text-transform: uppercase;
  color: var(--global-link-color, #52adc8);
}
.focus-challenge{
  list-style: none;
  margin: .1rem 0 0;
  padding: 0;
  width: 100%;
}
.focus-challenge li{
  position: relative;
  padding: .35rem 0 .35rem 1.15rem;
  font-size: .9rem;
  line-height: 1.55;
  color: var(--global-text-color);
}
.focus-challenge li::before{
  content: "";
  position: absolute;
  left: 0; top: .72rem;
  width: 7px; height: 7px;
  border-radius: 2px;
  transform: rotate(45deg);
  background: var(--global-link-color, #52adc8);
}
.focus-pubs{
  list-style: none;
  margin: .1rem 0 0;
  padding: 0;
}
.focus-pubs li{
  position: relative;
  padding: .42rem 0 .42rem 1.15rem;
  font-size: .87rem;
  line-height: 1.45;
  border-top: 1px solid var(--global-border-color, #eef2f3);
}
.focus-pubs li:first-child{ border-top: none; }
.focus-pubs li::before{
  content: "";
  position: absolute;
  left: 0; top: .78rem;
  width: 6px; height: 6px;
  border-radius: 50%;
  background: var(--global-link-color, #52adc8);
}
.focus-pubs a{
  color: var(--global-link-color, #52adc8);
  text-decoration: none;
  font-weight: 500;
}
.focus-pubs a:hover{ text-decoration: underline; }
.focus-pubs .focus-venue{
  color: var(--global-text-color-light, #8a949a);
  font-style: italic;
  font-size: .8rem;
}
.sciml-banner{
  display: flex;
  align-items: center;
  gap: .85rem;
  flex-wrap: wrap;
  margin: .2rem 0 .85rem;
  padding: .85rem 1.1rem;
  border-radius: 12px;
  background: linear-gradient(120deg, #2f7f93, #52adc8);
  box-shadow: 0 12px 28px -14px rgba(47,127,147,.65);
}
.sciml-tag{
  font-family: "Libre Franklin", "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-weight: 800;
  font-size: 1.32rem;
  line-height: 1.1;
  letter-spacing: -.01em;
  color: #fff;
}
.sciml-sub{
  font-size: .82rem;
  font-weight: 600;
  letter-spacing: .06em;
  text-transform: uppercase;
  color: rgba(255,255,255,.92);
  border-left: 2px solid rgba(255,255,255,.55);
  padding-left: .85rem;
}
.challenge-intro{
  font-size: .88rem;
  line-height: 1.6;
  color: var(--global-text-color);
  margin: .1rem 0 .3rem;
}
.challenge-intro strong{ color: #2f7f93; }
.challenge-grid{
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: .8rem;
  margin: .65rem 0 .2rem;
}
.challenge-block{
  margin: 0;
  padding: .95rem 1rem 1.05rem;
  border: 1px solid rgba(82,173,200,.35);
  border-top: 3px solid var(--global-link-color, #52adc8);
  border-radius: 11px;
  background: linear-gradient(180deg, rgba(82,173,200,.11), rgba(82,173,200,.03));
  box-shadow: 0 8px 20px -16px rgba(15,40,55,.55);
  transition: transform .2s ease, box-shadow .2s ease, border-color .2s ease;
}
.challenge-block:hover{
  transform: translateY(-3px);
  border-color: var(--global-link-color, #52adc8);
  box-shadow: 0 16px 30px -16px rgba(15,40,55,.55);
}
.challenge-head{ display: flex; align-items: center; gap: .55rem; }
.challenge-num{
  flex: 0 0 auto;
  width: 24px; height: 24px;
  border-radius: 7px;
  display: inline-flex; align-items: center; justify-content: center;
  background: var(--global-link-color, #52adc8);
  color: #fff; font-size: .78rem; font-weight: 800;
  box-shadow: 0 3px 8px -3px rgba(82,173,200,.8);
}
.challenge-name{ font-weight: 700; font-size: .88rem; line-height: 1.25; color: #23616f; }
.challenge-desc{ font-size: .78rem; line-height: 1.5; margin: .45rem 0 0; color: var(--global-text-color); }
@media (max-width: 600px){ .challenge-grid{ grid-template-columns: 1fr; } }
.focus-pub-tag{
  display: inline-block;
  font-size: .66rem; font-weight: 700; letter-spacing: .04em;
  text-transform: uppercase;
  color: var(--global-link-color, #52adc8);
  border: 1px solid var(--global-link-color, #52adc8);
  border-radius: 4px;
  padding: 0 .3rem;
  margin-left: .25rem;
  vertical-align: middle;
}
@media (max-width: 820px){ .focus-grid{ grid-template-columns: 1fr; } }
</style>

<div class="focus-grid">

  <details class="focus-card">
    <summary class="focus-summary">
      <span class="focus-head-row">
        <span class="focus-icon">&#9883;</span>
        <span class="focus-title">AI for Scientific Discovery</span>
        <span class="focus-chevron">&#9660;</span>
      </span>
      <span class="focus-blurb">We build physics-guided neural surrogates that faithfully model complex physical systems under severe data paucity, organized around four core research challenges.</span>
      <span class="focus-hint"><span class="focus-hint-more">Expand for challenges &amp; publications &#9660;</span><span class="focus-hint-less">Collapse &#9650;</span></span>
    </summary>
    <div class="focus-body">
      <div class="sciml-banner">
        <span class="sciml-tag">Parsimonious SciML</span>
        <span class="sciml-sub">Our lab's central research theme</span>
      </div>
      <p class="challenge-intro">We design neural surrogates that faithfully model complex physical systems under severe data paucity. This program is organized around four open challenges that stand between today's data-driven surrogates and trustworthy scientific deployment.</p>

      <span class="focus-section-label">Core Research Challenges</span>

      <div class="challenge-grid">
        <div class="challenge-block">
          <div class="challenge-head"><span class="challenge-num">1</span><span class="challenge-name">Rollout Error &amp; Spectral Bias</span></div>
          <p class="challenge-desc">Autoregressive neural surrogates accumulate error as they roll forward in time, while their spectral bias toward low frequencies leaves the fine-scale, high-frequency structure of physical fields under-resolved &mdash; eroding long-horizon fidelity.</p>
        </div>

        <div class="challenge-block">
          <div class="challenge-head"><span class="challenge-num">2</span><span class="challenge-name">Curse of (Simulation) Dimensionality</span></div>
          <p class="challenge-desc">The space of physical configurations, geometries, and parameters is enormous, while the high-fidelity simulations that generate training data are prohibitively costly &mdash; forcing surrogates to learn a high-dimensional map from only sparse samples.</p>
        </div>

        <div class="challenge-block">
          <div class="challenge-head"><span class="challenge-num">3</span><span class="challenge-name">Neural Surrogate Convergence Failures</span></div>
          <p class="challenge-desc">Physics-informed and constrained neural surrogates are notoriously hard to optimize: stiff loss landscapes, initialization sensitivity, and competing objectives cause training to stall or converge to non-physical solutions.</p>
        </div>

        <div class="challenge-block">
          <div class="challenge-head"><span class="challenge-num">4</span><span class="challenge-name">Extrapolation Failure</span></div>
          <p class="challenge-desc">Surrogates that interpolate well within their training regime break down when asked to generalize to unseen parameters, geometries, or dynamical regimes &mdash; precisely the setting scientific deployment most demands.</p>
        </div>
      </div>

      <span class="focus-section-label">Related Publications</span>
      <ul class="focus-pubs">
        <li><a href="https://arxiv.org/abs/2607.00196">TRIE: An Evaluation Framework for Stochastic PDE Surrogates</a> <span class="focus-venue">— arXiv</span> <span class="focus-pub-tag">preprint</span></li>
        <li><a href="https://arxiv.org/abs/2607.14233">LIGO-PINN: Learned Initialization via Gated Optimization to Alleviate Convergence Failures in Physics-Informed Neural Networks</a> <span class="focus-venue">— arXiv</span> <span class="focus-pub-tag">preprint</span></li>
        <li><a href="https://arxiv.org/abs/2601.20884">Finetune-Informed Pretraining Boosts Downstream Performance</a> <span class="focus-venue">— arXiv</span> <span class="focus-pub-tag">preprint</span></li>
        <li><a href="https://www.sciencedirect.com/science/article/abs/pii/S0032591025006734">Learning and Interpreting Drag Force Models for Dense Particle Suspensions Using Graph Neural Networks</a> <span class="focus-venue">— Powder Technology 2025</span></li>
        <li><a href="https://doi.org/10.1016/j.fluid.2025.114646">Science-Guided Transfer Learning for Molecular Dynamics of Confined Fluids in Shale Nanopores</a> <span class="focus-venue">— Fluid Phase Equilibria 2025</span></li>
        <li><a href="https://arxiv.org/abs/2503.10048">Model-Agnostic Knowledge Guided Correction for Improved Neural Surrogate Rollout</a> <span class="focus-venue">— ICLR 2025</span></li>
        <li><a href="https://ieeexplore.ieee.org/document/10825483">Counter Data Paucity through Adversarial Invariance Encoding: A Case Study on Battery Thermal Runaway</a> <span class="focus-venue">— IEEE Big Data 2024</span></li>
        <li><a href="https://ojs.aaai.org/index.php/AAAI/article/view/29428">Reinforcement Learning as a Parsimonious Alternative to Prediction Cascades</a> <span class="focus-venue">— AAAI 2024</span></li>
        <li><a href="https://www.sciencedirect.com/science/article/abs/pii/S0032591024003267">Physics Informed Deep Learning for Flow and Force Predictions in Dense Ellipsoidal Particle Suspensions</a> <span class="focus-venue">— Powder Technology 2024</span></li>
        <li><a href="https://pubs.aip.org/aip/pof/article/35/7/073330/2904208/Comparison-of-reduced-order-models-based-on">Comparison of Reduced Order Models Based on Dynamic Mode Decomposition</a> <span class="focus-venue">— Physics of Fluids 2023</span></li>
        <li><a href="https://www.sciencedirect.com/science/article/abs/pii/S0032591022001978">Deep Learning Methods for Predicting Fluid Forces in Dense Particle Suspensions</a> <span class="focus-venue">— Powder Technology 2022</span></li>
        <li><a href="https://ieeexplore.ieee.org/document/9679054/">PhyFlow: Physics-Guided Deep Learning for Generating Interpretable 3D Flow Fields</a> <span class="focus-venue">— IEEE ICDM 2021</span></li>
        <li><a href="https://www.liebertpub.com/doi/10.1089/big.2020.0071">Physics-Guided Deep Learning for Drag Force Prediction in Dense Fluid-Particulate Systems</a> <span class="focus-venue">— Big Data 2020</span></li>
        <li><a href="https://epubs.siam.org/doi/abs/10.1137/1.9781611976236.63">PhyNet: Physics Guided Neural Networks for Particle Drag Force Prediction in Assembly</a> <span class="focus-venue">— SIAM SDM 2020</span></li>
      </ul>
    </div>
  </details>

  <details class="focus-card">
    <summary class="focus-summary">
      <span class="focus-head-row">
        <span class="focus-icon">
          <!-- Powered microchip: silicon metering electricity, i.e. a cyber-physical system -->
          <svg viewBox="0 0 24 24" role="img" aria-label="Microchip carrying an electrical charge" focusable="false">
            <rect x="5.5" y="5.5" width="13" height="13" rx="2.5" />
            <path d="M9 2.5v3M15 2.5v3M9 18.5v3M15 18.5v3M2.5 9h3M2.5 15h3M18.5 9h3M18.5 15h3" />
            <path d="M13 8.5 10 12.3h2.6L11.6 15.8l3.2-4.1h-2.6z" stroke-width="1.1" />
          </svg>
        </span>
        <span class="focus-title">AI for Cyber-Physical Systems</span>
        <span class="focus-chevron">&#9660;</span>
      </span>
      <span class="focus-blurb">We learn system invariants and detect anomalies, adversarial attacks, and faults in the noisy, real-time sensor and wireless data streams that cyber-physical systems produce.</span>
      <span class="focus-hint"><span class="focus-hint-more">Expand for challenges &amp; publications &#9660;</span><span class="focus-hint-less">Collapse &#9650;</span></span>
    </summary>
    <div class="focus-body">
      <span class="focus-section-label">Related Publications</span>
      <ul class="focus-pubs">
        <li><a href="https://dl.acm.org/doi/10.1145/3066167">ILLIAD: Intelligent Invariant and Anomaly Detection in Cyber-Physical Systems</a> <span class="focus-venue">— ACM TIST 2018</span></li>
        <li><a href="https://ieeexplore.ieee.org/document/8621955/">Incorporating Prior Domain Knowledge into Deep Neural Networks</a> <span class="focus-venue">— IEEE Big Data 2018</span></li>
        <li><a href="https://ieeexplore.ieee.org/document/8999069/">Detection of False Data Injection Attacks in Cyber-Physical Systems Using Dynamic Invariants</a> <span class="focus-venue">— IEEE ICMLA 2019</span></li>
        <li><a href="https://ieeexplore.ieee.org/document/9702276/">Contrastive Graph Convolutional Networks for Hardware Trojan Detection</a> <span class="focus-venue">— IEEE HOST 2021</span></li>
        <li><a href="https://ieeexplore.ieee.org/document/10017520/">Efficient Generative Wireless Anomaly Detection for Next Generation Networks</a> <span class="focus-venue">— IEEE MILCOM 2022</span></li>
        <li><a href="https://ieeexplore.ieee.org/document/10027665/">Detecting Irregular Network Activity with Adversarial Learning and Expert Feedback</a> <span class="focus-venue">— IEEE ICDM 2022</span></li>
        <li><a href="https://ieeexplore.ieee.org/document/10599304/">Large Multi-Modal Models (LMMs) as Universal Foundation Models for AI-Native Wireless Systems</a> <span class="focus-venue">— IEEE Network 2024</span></li>
        <li><a href="https://ieeexplore.ieee.org/document/10786062/">NMformer: A Transformer for Noisy Modulation Classification in Wireless Communication</a> <span class="focus-venue">— IEEE WOCC 2024</span></li>
        <li><a href="https://ieeexplore.ieee.org/document/11005616/">DenoMAE: A Multimodal Autoencoder for Denoising Modulation Signals</a> <span class="focus-venue">— IEEE Communications Letters 2025</span></li>
        <li><a href="https://ieeexplore.ieee.org/document/11218877/">DenoMAE2.0: Improving Denoising Masked Autoencoders by Classifying Local Patches</a> <span class="focus-venue">— IEEE Transactions on Communications 2025</span></li>
      </ul>
    </div>
  </details>

  <details class="focus-card">
    <summary class="focus-summary">
      <span class="focus-head-row">
        <span class="focus-icon">&#128200;</span>
        <span class="focus-title">Spatiotemporal and Disease Modeling</span>
        <span class="focus-chevron">&#9660;</span>
      </span>
      <span class="focus-blurb">We design attention-based and sequence-to-sequence models for long-horizon forecasting, disease modeling, and interpretable analysis of complex, high-dimensional dynamical systems.</span>
      <span class="focus-hint"><span class="focus-hint-more">Expand for challenges &amp; publications &#9660;</span><span class="focus-hint-less">Collapse &#9650;</span></span>
    </summary>
    <div class="focus-body">
      <span class="focus-section-label">Related Publications</span>
      <ul class="focus-pubs">
        <li><a href="https://ieeexplore.ieee.org/abstract/document/7372200">Recommending Temporally Relevant News Content from Implicit Feedback Data</a> <span class="focus-venue">— IEEE ICTAI 2015</span></li>
        <li><a href="https://www.ijcai.org/proceedings/2019/441">DyAt Nets: Dynamic Attention Networks for State Forecasting in Cyber-Physical Systems</a> <span class="focus-venue">— IJCAI 2019</span></li>
        <li><a href="https://ieeexplore.ieee.org/document/9005511/">Multivariate Long-Term State Forecasting in Cyber-Physical Systems: A Sequence to Sequence Approach</a> <span class="focus-venue">— IEEE Big Data 2019</span></li>
        <li><a href="https://dl.acm.org/doi/abs/10.1145/3394118">Cut-n-Reveal: Time Series Segmentations with Explanations</a> <span class="focus-venue">— ACM TIST 2020</span></li>
        <li><a href="https://ojs.aaai.org/index.php/AAAI/article/view/16618">Steering a Historical Disease Forecasting Model Under a Pandemic</a> <span class="focus-venue">— AAAI 2021</span></li>
        <li><a href="https://www.nature.com/articles/s41467-024-50601-9">Evaluation of FluSight Influenza Forecasting in the 2021&ndash;22 and 2022&ndash;23 Seasons</a> <span class="focus-venue">— Nature Communications 2024</span></li>
      </ul>
    </div>
  </details>

</div>

<style>
.members-grid{
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1.25rem;
  margin: 0 0 2rem;
}
.member-card{
  display: flex;
  flex-direction: column;
  align-self: start;
  text-align: center;
  padding: 1.4rem 1rem 1.25rem;
  background: linear-gradient(0deg, rgba(82,173,200,.02), rgba(82,173,200,.04));
  border: 1px solid var(--global-border-color, #e3e8ea);
  border-top: 4px solid var(--global-link-color, #52adc8);
  border-radius: 14px;
  transition: box-shadow .25s ease, transform .25s ease, border-color .25s ease;
}
.member-card:hover{
  border-color: var(--global-link-color, #52adc8);
  box-shadow: 0 14px 30px -18px rgba(15,40,55,.45);
  transform: translateY(-2px);
}
.member-thumb{
  width: 104px; height: 104px;
  border-radius: 50%;
  object-fit: cover;
  display: block;
  margin: 0 auto .9rem;
  border: 1px solid var(--global-border-color, #dfe6e8);
  background: #eef2f3;
}
.member-name{ font-weight: 700; font-size: 1.02rem; line-height: 1.25; color: #23616f; }
.member-email{ font-size: .9rem; margin-top: .15rem; }
.member-email a{ color: var(--global-link-color-hover, #2f7f93); text-decoration: none; font-weight: 500; }
.member-email a:hover{ text-decoration: underline; }
.member-dates{ font-size: .85rem; margin-top: .2rem; color: #566069; }
.member-note{ font-size: .85rem; margin-top: .3rem; color: var(--global-text-color); }
.member-thesis{
  font-size: .76rem; line-height: 1.45; margin-top: .55rem;
  color: #4f5962; font-style: italic;
}
.member-more{ margin-top: .7rem; }
.member-more summary{
  cursor: pointer;
  list-style: none;
  display: inline-block;
  font-size: .78rem; font-weight: 600; letter-spacing: .02em;
  color: var(--global-link-color);
  padding: .15rem .2rem;
}
.member-more summary::-webkit-details-marker{ display: none; }
.member-more summary::after{ content: "  ▾"; font-size: .7em; }
.member-more[open] summary::after{ content: "  ▴"; }
.member-bio{
  text-align: left;
  font-size: .85rem; line-height: 1.55;
  margin: .55rem 0 0;
  padding-top: .55rem;
  border-top: 1px solid var(--global-border-color, #e3e8ea);
  color: var(--global-text-color);
}
@media (max-width: 768px){ .members-grid{ grid-template-columns: repeat(2, 1fr); } }
@media (max-width: 480px){ .members-grid{ grid-template-columns: 1fr; } }
</style>

Members
======

Ph.D Students
-------------

<div class="members-grid">
  <div class="member-card">
    <img class="member-thumb" src="/images/members/bharat-srikishan.jpg" onerror="this.onerror=null;this.src='/images/members/placeholder.svg'" alt="Bharat Srikishan">
    <div class="member-name">Bharat Srikishan</div>
    <div class="member-email"><a href="mailto:bsrikish@stevens.edu">bsrikish@stevens.edu</a></div>
    <div class="member-dates">(2022 - present)</div>
    <details class="member-more">
      <summary>Research</summary>
      <p class="member-bio">Bharat's research is focused on developing machine learning techniques with a focus on improved generalization under data paucity and compute paucity contexts. Bharat's research has been published in prestigious venues like AAAI and ICLR.</p>
    </details>
  </div>
  <div class="member-card">
    <img class="member-thumb" src="/images/members/reihaneh-roshan.jpg" onerror="this.onerror=null;this.src='/images/members/placeholder.svg'" alt="Reihaneh Gh. Roshan">
    <div class="member-name">Reihaneh Gh. Roshan</div>
    <div class="member-email"><a href="mailto:rghasemi@stevens.edu">rghasemi@stevens.edu</a></div>
    <div class="member-dates">(2023 - present)</div>
    <details class="member-more">
      <summary>Research</summary>
      <p class="member-bio">Research summary coming soon.</p>
    </details>
  </div>
  <div class="member-card">
    <img class="member-thumb" src="/images/members/shital-adhikari.jpg" onerror="this.onerror=null;this.src='/images/members/placeholder.svg'" alt="Shital Adhikari">
    <div class="member-name">Shital Adhikari</div>
    <div class="member-email"><a href="mailto:sadhikar1@stevens.edu">sadhikar1@stevens.edu</a></div>
    <div class="member-dates">(2024 - present)</div>
    <details class="member-more">
      <summary>Research</summary>
      <p class="member-bio">Research summary coming soon.</p>
    </details>
  </div>
</div>

M.S. Students
-------------

<div class="members-grid">
  <div class="member-card">
    <img class="member-thumb" src="/images/members/nilay-anurag.jpg" onerror="this.onerror=null;this.src='/images/members/placeholder.svg'" alt="Nilay Anurag">
    <div class="member-name">Nilay Anurag</div>
    <div class="member-email"><a href="mailto:nanurag@stevens.edu">nanurag@stevens.edu</a></div>
    <div class="member-dates">(2022 - 2025)</div>
    <div class="member-thesis">M.S. Thesis: "Improving Prediction Performance in Physics-Informed Machine Learning Through Pre-Training and Adaptation"</div>
    <details class="member-more">
      <summary>Research</summary>
      <p class="member-bio">Research summary coming soon.</p>
    </details>
  </div>
  <div class="member-card">
    <img class="member-thumb" src="/images/members/ali-el-sayed.jpg" onerror="this.onerror=null;this.src='/images/members/placeholder.svg'" alt="Ali El Sayed">
    <div class="member-name">Ali El Sayed</div>
    <div class="member-email"><a href="mailto:aelsaye1@stevens.edu">aelsaye1@stevens.edu</a></div>
    <div class="member-dates">(2023 - 2025)</div>
    <div class="member-thesis">M.S. Thesis: "LLM-Modulo-Rec: Leveraging Approximate World-Knowledge of LLMs to Improve eCommerce Search Ranking Under Data Paucity"</div>
    <details class="member-more">
      <summary>Research</summary>
      <p class="member-bio">Research summary coming soon.</p>
    </details>
  </div>
  <div class="member-card">
    <img class="member-thumb" src="/images/members/sai-sathwik-abbaraju.jpg" onerror="this.onerror=null;this.src='/images/members/placeholder.svg'" alt="Sai Sathwik Abbaraju">
    <div class="member-name">Sai Sathwik Abbaraju</div>
    <div class="member-email"><a href="mailto:sabbaraj@stevens.edu">sabbaraj@stevens.edu</a></div>
    <div class="member-dates">(2024 - present)</div>
    <div class="member-thesis">Research: "Neuro-Mechanistic Modeling for Compute-Efficient Scientific Modeling"</div>
    <details class="member-more">
      <summary>Research</summary>
      <p class="member-bio">Research summary coming soon.</p>
    </details>
  </div>
</div>

High School Students
--------------------

<div class="members-grid">
  <div class="member-card">
    <img class="member-thumb" src="/images/members/ishaan-sinha.jpg" onerror="this.onerror=null;this.src='/images/members/placeholder.svg'" alt="Ishaan Sinha">
    <div class="member-name">Ishaan Sinha</div>
    <div class="member-note">Current: B.S. @ Harvard</div>
    <details class="member-more">
      <summary>Research</summary>
      <p class="member-bio">Research summary coming soon.</p>
    </details>
  </div>
  <div class="member-card">
    <img class="member-thumb" src="/images/members/riddhi-ganesh.jpg" onerror="this.onerror=null;this.src='/images/members/placeholder.svg'" alt="Riddhi Ganesh">
    <div class="member-name">Riddhi Ganesh</div>
    <details class="member-more">
      <summary>Research</summary>
      <p class="member-bio">Research summary coming soon.</p>
    </details>
  </div>
  <div class="member-card">
    <img class="member-thumb" src="/images/members/arya-vaidya.jpg" onerror="this.onerror=null;this.src='/images/members/placeholder.svg'" alt="Arya Vaidya">
    <div class="member-name">Arya Vaidya</div>
    <div class="member-note">Current: B.S. @ Georgia Tech</div>
    <details class="member-more">
      <summary>Research</summary>
      <p class="member-bio">Research summary coming soon.</p>
    </details>
  </div>
</div>
