---
permalink: /projects/
title: false
author_profile: false
classes: wide
---

<style>
/* widen the content shell for this gallery page */
#main{ max-width: 1280px; }
#main .page{ float: none; clear: both; width: 100%; margin: 0; padding: 0; }
#main .page__inner-wrap{ margin: 0; }

.proj-page{
  --accent: var(--global-base-color, #2f7f93);
  --ink: var(--global-text-color, #4b5158);
  --surface: color-mix(in srgb, var(--global-bg-color, #fff) 97%, var(--accent));
  --hairline: color-mix(in srgb, var(--accent) 18%, transparent);
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 1.25rem 4rem;
}

/* ---- Page header ---- */
.proj-hero{
  padding: 1.5rem 0 2.25rem;
  border-bottom: 1px solid var(--hairline);
  margin-bottom: 2.75rem;
}
.proj-hero .eyebrow{
  font-family: "IBM Plex Mono", ui-monospace, monospace;
  font-size: .72rem; letter-spacing: .28em; text-transform: uppercase;
  color: var(--accent); margin: 0 0 .9rem;
}
.proj-hero h1{
  font-family: "Libre Franklin", "Helvetica Neue", Helvetica, Arial, sans-serif; font-weight: 700;
  font-size: clamp(2.1rem, 5vw, 3.25rem); line-height: 1.12;
  letter-spacing: -.02em; margin: 0 0 1rem; color: var(--global-text-color);
  padding-bottom: .04em;
}
.proj-hero p{
  max-width: 80%; font-size: 1.05rem; line-height: 1.6;
  color: color-mix(in srgb, var(--ink) 80%, transparent); margin: 0;
}

/* ---- Grid: 4 cards per row ---- */
.proj-grid{
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1.5rem;
}

/* ---- Card ---- */
.pcard{
  display: flex;
  flex-direction: column;
  position: relative;
  background: var(--surface);
  border: 1px solid var(--hairline);
  border-radius: 14px;
  overflow: hidden;
  text-decoration: none;
  color: inherit;
  box-shadow: 0 1px 2px rgba(15,30,40,.04);
  transition: transform .3s cubic-bezier(.2,.7,.2,1), box-shadow .3s ease, border-color .3s ease;
  will-change: transform;
}
.pcard:hover{
  transform: scale(1.58);              /* ~2.5x the card's area on hover */
  z-index: 10;
  box-shadow: 0 30px 60px -20px rgba(15,40,55,.55);
  border-color: color-mix(in srgb, var(--accent) 45%, transparent);
}
/* anchor edge columns so the magnified card stays on-screen (3-col layout) */
.pcard:nth-child(3n+1):hover{ transform-origin: left center; }
.pcard:nth-child(3n+2):hover{ transform-origin: center; }
.pcard:nth-child(3n):hover{ transform-origin: right center; }

/* figure */
.pcard-fig{
  height: 132px;
  background: #fff;
  border-bottom: 1px solid color-mix(in srgb, var(--accent) 12%, transparent);
  display: flex; align-items: center; justify-content: center;
  padding: .65rem;
}
.pcard-fig img{ max-width: 100%; max-height: 100%; object-fit: contain; display: block; }
.pcard-fig--empty{
  font-family: "Libre Franklin", "Helvetica Neue", Helvetica, Arial, sans-serif; font-style: italic;
  color: color-mix(in srgb, var(--accent) 55%, transparent);
  font-size: 1.4rem;
}

/* body */
.pcard-body{ display: flex; flex-direction: column; flex: 1; padding: 1.05rem 1.1rem 1.15rem; }
.pcard-meta{ display: flex; align-items: center; gap: .55rem; margin-bottom: .55rem; }
.pcard-num{
  font-family: "IBM Plex Mono", ui-monospace, monospace; font-size: .72rem; font-weight: 600;
  color: var(--accent); padding: .08rem .42rem; border: 1px solid var(--hairline);
  border-radius: 5px; letter-spacing: .04em;
}
.pcard-venue{
  font-family: "IBM Plex Mono", ui-monospace, monospace; font-size: .6rem;
  letter-spacing: .14em; text-transform: uppercase;
  color: color-mix(in srgb, var(--ink) 62%, transparent);
}
.pcard-title{
  font-family: "Libre Franklin", "Helvetica Neue", Helvetica, Arial, sans-serif; font-weight: 600;
  font-size: 1.02rem; line-height: 1.22; letter-spacing: -.01em;
  margin: 0 0 .55rem; color: var(--global-text-color);
  display: -webkit-box; -webkit-line-clamp: 3; -webkit-box-orient: vertical; overflow: hidden;
}
.pcard-desc{
  font-size: .82rem; line-height: 1.5;
  color: color-mix(in srgb, var(--ink) 85%, transparent); margin: 0 0 .9rem;
  display: -webkit-box; -webkit-line-clamp: 5; -webkit-box-orient: vertical; overflow: hidden;
}
.pcard-cta{
  margin-top: auto;
  font-family: "IBM Plex Mono", ui-monospace, monospace; font-size: .72rem;
  letter-spacing: .04em; color: var(--accent);
}
/* Cards with more than one destination: a row of links instead of one CTA. */
.pcard-links{
  margin-top: auto;
  display: flex; flex-wrap: wrap; gap: 1.1rem;
}
.pcard-links .pcard-cta{
  margin-top: 0;
  text-decoration: none;
  border-bottom: 1px solid color-mix(in srgb, var(--accent) 30%, transparent);
}
.pcard-links .pcard-cta:hover{
  border-bottom-color: var(--accent);
}
.pcard-links .pcard-cta::after{ content: " →"; }
/*
 * Clicking anywhere on the card opens the paper. The paper link stretches an
 * invisible overlay across the whole card; the code link is lifted above it so
 * it keeps its own target. (Nesting <a> inside <a> is invalid HTML, hence this.)
 */
.pcard-cta--paper::before{
  content: "";
  position: absolute;
  inset: 0;
  z-index: 1;
}
.pcard-cta--code{
  position: relative;
  z-index: 2;
}
.pcard-cta::after{ content: " →"; transition: margin-left .25s ease; }
.pcard:hover .pcard-cta::after{ margin-left: .25rem; }

/* ---- Responsive (reflexive) ---- */
@media (max-width: 820px){
  .proj-grid{ grid-template-columns: repeat(2, 1fr); }
  .pcard:hover{ transform: scale(1.45); }  /* a touch smaller so 2-up zoom fits */
  .pcard:nth-child(2n+1):hover{ transform-origin: left center; }
  .pcard:nth-child(2n):hover{ transform-origin: right center; }
}
@media (max-width: 540px){
  .proj-grid{ grid-template-columns: 1fr; }
  .pcard:hover{ transform: scale(1.03); transform-origin: center; }
  .pcard-fig{ height: 170px; }
  .pcard-desc{ -webkit-line-clamp: 6; }
}
</style>

<div class="proj-page" markdown="0">

  <header class="proj-hero">
    <p class="eyebrow">ScAILab &middot; Research</p>
    <h1>Selected Research Projects</h1>
    <p>Representative work from the Scientific Artificial Intelligence Lab, spanning physics-guided deep learning, anomaly detection, and disease forecasting under data paucity. Hover a card to magnify it; click to open the paper or code.</p>
  </header>

  <div class="proj-grid">

    <div class="pcard">
      <div class="pcard-fig"><img src="/images/projects/ligo-pinn.jpg" alt="LIGO-PINN evaluation domains: heat transfer, fluid dynamics and wave propagation"></div>
      <div class="pcard-body">
        <div class="pcard-meta"><span class="pcard-num">01</span><span class="pcard-venue">arXiv 2026</span></div>
        <h3 class="pcard-title">LIGO-PINN: Learned Initialization via Gated Optimization to Alleviate Convergence Failures in Physics Informed Neural Networks</h3>
        <p class="pcard-desc">Physics-informed neural networks often converge poorly, sometimes to trivial solutions, on challenging PDE domains. LIGO-PINN traces these catastrophic failures to network initialization, a surprisingly under-investigated factor, and learns the initial weights through gated layerwise optimization. Across 1D and 2D domains including a challenging 2D fluid dynamics setting, it improves on six state-of-the-art baselines by 91.5% on average and generalizes to 3D unstructured domains.</p>
        <div class="pcard-links">
          <a class="pcard-cta pcard-cta--paper" href="https://arxiv.org/pdf/2607.14233" target="_blank" rel="noopener noreferrer">Read paper</a>
          <a class="pcard-cta pcard-cta--code" href="https://github.com/scailab/ligo-pinn" target="_blank" rel="noopener noreferrer">View code</a>
        </div>
      </div>
    </div>

    <div class="pcard">
      <div class="pcard-fig"><img src="/images/projects/trie.png" alt="TRIE evaluation framework: trustworthiness, invariance and efficiency criteria"></div>
      <div class="pcard-body">
        <div class="pcard-meta"><span class="pcard-num">02</span><span class="pcard-venue">arXiv 2026</span></div>
        <h3 class="pcard-title">TRIE: An Evaluation Framework for Stochastic PDE Surrogates</h3>
        <p class="pcard-desc">An evaluation framework for stochastic PDE surrogates that asks whether models reproduce invariant measures, provide trustworthy predictive uncertainty, and scale to efficient probabilistic generation. Across stochastic Kuramoto&ndash;Sivashinsky and Kolmogorov flow at 11 parameter values, pointwise-trained surrogates give plausible short rollouts but miss long-time statistics, while generative models achieve the lowest CRPS. Latent generative models cut Kolmogorov inference time by roughly 12&times;.</p>
        <div class="pcard-links">
          <a class="pcard-cta pcard-cta--paper" href="https://arxiv.org/pdf/2607.00196" target="_blank" rel="noopener noreferrer">Read paper</a>
          <a class="pcard-cta pcard-cta--code" href="https://github.com/scailab/TRIE-SPDE-Bench" target="_blank" rel="noopener noreferrer">View code</a>
        </div>
      </div>
    </div>

    <div class="pcard">
      <div class="pcard-fig"><img src="/images/projects/hyper.png" alt="HyPER rollout: a decision function choosing between neural surrogate and PDE simulator"></div>
      <div class="pcard-body">
        <div class="pcard-meta"><span class="pcard-num">03</span><span class="pcard-venue">ICLR 2025</span></div>
        <h3 class="pcard-title">Model-Agnostic Knowledge Guided Correction for Improved Neural Surrogate Rollout</h3>
        <p class="pcard-desc">Neural surrogates are far cheaper than PDE simulators but accumulate large rollout error when run autoregressively, especially under data paucity. HyPER is a model-agnostic, cost-aware reinforcement learning model that decides when to invoke a physics simulator, with or without gradients, to correct a neural surrogate. It reduces in-distribution rollout error by 47&ndash;78% and learns a policy that adapts to changing physical conditions and resists noise corruption.</p>
        <div class="pcard-links">
          <a class="pcard-cta pcard-cta--paper" href="https://arxiv.org/pdf/2503.10048" target="_blank" rel="noopener noreferrer">Read paper</a>
          <a class="pcard-cta pcard-cta--code" href="https://github.com/scailab/HyPER" target="_blank" rel="noopener noreferrer">View code</a>
        </div>
      </div>
    </div>

    <div class="pcard">
      <div class="pcard-fig"><img src="/images/projects/paser.png" alt="PaSeR: parsimonious segmentation with reinforcement learning"></div>
      <div class="pcard-body">
        <div class="pcard-meta"><span class="pcard-num">04</span><span class="pcard-venue">AAAI 2024</span></div>
        <h3 class="pcard-title">Reinforcement Learning as a Parsimonious Alternative to Prediction Cascades: A Case Study on Image Segmentation</h3>
        <p class="pcard-desc">Over-parameterized vision architectures are infeasible in low-resource IoT settings, and decision cascades waste computation on intermediate models. PaSeR is a non-cascading, cost-aware learning pipeline that reaches better accuracy at lower cost. Evaluated with a new IoU/GigaFlop metric, it improves by at least 174% on battery material phase segmentation and 13.4% over state-of-the-art models on noisy MNIST.</p>
        <div class="pcard-links">
          <a class="pcard-cta pcard-cta--paper" href="https://arxiv.org/pdf/2402.11760" target="_blank" rel="noopener noreferrer">Read paper</a>
          <a class="pcard-cta pcard-cta--code" href="https://github.com/scailab/paser" target="_blank" rel="noopener noreferrer">View code</a>
        </div>
      </div>
    </div>

    <div class="pcard">
      <div class="pcard-fig"><img src="/images/projects/caad.png" alt="CAAD framework"></div>
      <div class="pcard-body">
        <div class="pcard-meta"><span class="pcard-num">05</span><span class="pcard-venue">ICDM 2022</span></div>
        <h3 class="pcard-title">Detecting Irregular Network Activity with Adversarial Learning and Expert Feedback</h3>
        <p class="pcard-desc">A self-supervised deep learning framework, CAAD, for anomaly detection in wireless communication systems. It uses contrastive learning in an adversarial setup to learn representations of normal and anomalous behavior, yielding a 92.84% mean performance improvement over state-of-the-art techniques. An augmented variant (CAAD-EF) incorporates expert feedback through a contrastive feedback loop to reduce prediction uncertainty.</p>
        <div class="pcard-links">
          <a class="pcard-cta pcard-cta--paper" href="https://arxiv.org/abs/2210.02841" target="_blank" rel="noopener noreferrer">Read paper</a>
          <a class="pcard-cta pcard-cta--code" href="https://github.com/rgopikrishna-vt/CAAD" target="_blank" rel="noopener noreferrer">View code</a>
        </div>
      </div>
    </div>

    <a class="pcard" href="https://ieeexplore.ieee.org/document/9679054">
      <div class="pcard-fig"><img src="/images/projects/phyflow.jpg" alt="PhyFlow architecture"></div>
      <div class="pcard-body">
        <div class="pcard-meta"><span class="pcard-num">06</span><span class="pcard-venue">IEEE ICDM 2021</span></div>
        <h3 class="pcard-title">PhyFlow: Physics-Guided Deep Learning for Generating Interpretable 3D Flow Fields</h3>
        <p class="pcard-desc">A physics-guided deep learning architecture for modeling 3D multi-phase fluid flows, designed to mimic the projection method used in CFD simulations. PhyFlow generates high-quality flow fields with a 49.61% improvement over state-of-the-art baselines, improves downstream particle drag force prediction by 9.89%, and remains consistent with known governing equations.</p>
        <span class="pcard-cta">Read paper</span>
      </div>
    </a>

    <div class="pcard">
      <div class="pcard-fig"><img src="/images/projects/cali-net.png" alt="CALI-Net architecture"></div>
      <div class="pcard-body">
        <div class="pcard-meta"><span class="pcard-num">07</span><span class="pcard-venue">AAAI 2021</span></div>
        <h3 class="pcard-title">Steering a Historical Disease Forecasting Model Under a Pandemic</h3>
        <p class="pcard-desc">CALI-Net is a neural transfer learning architecture that uses knowledge distillation to "steer" a historical disease forecasting model into scenarios where flu and COVID-19 co-exist. It learns to emphasize either COVID-related signals or historical forecasting models at appropriate times, exploiting historical ILI representations alongside limited COVID-related signals.</p>
        <div class="pcard-links">
          <a class="pcard-cta pcard-cta--paper" href="https://arxiv.org/abs/2009.11407" target="_blank" rel="noopener noreferrer">Read paper</a>
          <a class="pcard-cta pcard-cta--code" href="https://github.com/AdityaLab/CALI-Net" target="_blank" rel="noopener noreferrer">View code</a>
        </div>
      </div>
    </div>

    <a class="pcard" href="https://epubs.siam.org/doi/pdf/10.1137/1.9781611976236.63">
      <div class="pcard-fig"><img src="/images/projects/phynet.png" alt="PhyNet architecture"></div>
      <div class="pcard-body">
        <div class="pcard-meta"><span class="pcard-num">08</span><span class="pcard-venue">SIAM SDM 2020</span></div>
        <h3 class="pcard-title">PhyNet: Physics Guided Neural Networks for Particle Drag Force Prediction</h3>
        <p class="pcard-desc">A deep learning model using physics-guided structural priors and physics-guided aggregate supervision to model the drag forces acting on each particle in a Computational Fluid Dynamics-Discrete Element Method (CFD-DEM) setup. Extensive experiments showcase the value of incorporating physics knowledge directly into the learning formulation under data paucity.</p>
        <span class="pcard-cta">Read paper</span>
      </div>
    </a>

    <a class="pcard" href="https://dl.acm.org/doi/epdf/10.1145/3394118">
      <div class="pcard-fig"><img src="/images/projects/cnr.png" alt="Cut-n-Reveal framework"></div>
      <div class="pcard-body">
        <div class="pcard-meta"><span class="pcard-num">09</span><span class="pcard-venue">ACM TIST 2020</span></div>
        <h3 class="pcard-title">Cut-n-Reveal: Temporal Segmentation with Explanations</h3>
        <p class="pcard-desc">CnR is a scalable segmentation-with-explanations framework that segments power-outage sequences based on temporal variations in the failure process, accounting for spatial and temporal correlations. A novel explanation optimization highlights the culprit time-series behind each segment. On real county-level outage data from hurricanes Matthew, Harvey, and Irma, CnR recovers actionable patterns baselines miss.</p>
        <span class="pcard-cta">Read paper</span>
      </div>
    </a>

    <a class="pcard" href="https://people.cs.vt.edu/ramakris/papers/PID5657885.pdf">
      <div class="pcard-fig"><img src="/images/projects/dann.png" alt="DANN framework"></div>
      <div class="pcard-body">
        <div class="pcard-meta"><span class="pcard-num">10</span><span class="pcard-venue">IEEE Big Data 2018</span></div>
        <h3 class="pcard-title">Incorporating Prior Domain Knowledge into Deep Neural Networks</h3>
        <p class="pcard-desc">Domain Adapted Neural Networks (DANN) integrate domain knowledge into model training via loss terms for monotonicity and approximation constraints. Evaluated on synthetic Bohachevsky data and a real-world oxygen-solubility dataset, DANN outperforms its domain-agnostic counterpart with an overall mean performance improvement of 19.5% (4% worst-case, 42.7% best-case).</p>
        <span class="pcard-cta">Read paper</span>
      </div>
    </a>

    <a class="pcard" href="https://people.cs.vt.edu/ramakris/papers/illiad-tist2017.pdf">
      <div class="pcard-fig"><img src="/images/projects/illiad.png" alt="illiad system"></div>
      <div class="pcard-body">
        <div class="pcard-meta"><span class="pcard-num">11</span><span class="pcard-venue">ACM TIST 2018</span></div>
        <h3 class="pcard-title">illiad: Intelligent Invariant and Anomaly Detection in Cyber-Physical Systems</h3>
        <p class="pcard-desc">An online monitoring system that models the state of a cyber-physical system as a function of relationships between its constituent components, combining model-based and data-driven strategies. illiad exploits the underlying network structure (wired or wireless) for state estimation, demonstrated on a wireless sensor motes application and an IEEE 33-bus microgrid.</p>
        <span class="pcard-cta">Read paper</span>
      </div>
    </a>


  </div>
</div>
