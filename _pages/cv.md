---
layout: archive
title: "CV"
permalink: /cv/
author_profile: false
redirect_from:
  - /resume
---

{% include base_path %}

<style>
.cv-actions{
  --accent: var(--global-base-color, #2f7f93);
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  gap: .75rem;
  margin: 0 0 1.25rem;
}
.cv-actions a{
  display: inline-block;
  font-family: "Libre Franklin", "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-size: .86rem;
  font-weight: 600;
  letter-spacing: .02em;
  text-decoration: none;
  padding: .5rem .95rem;
  border-radius: 8px;
  border: 1px solid color-mix(in srgb, var(--accent) 35%, transparent);
  color: var(--accent);
  background: color-mix(in srgb, var(--accent) 7%, transparent);
}
.cv-actions a:hover{
  background: color-mix(in srgb, var(--accent) 14%, transparent);
  text-decoration: none;
}
/*
 * The viewer's own dark page-gutter lives inside the plugin and can't be styled
 * from here. Fitting pages to the frame width (#view=FitH) leaves only thin
 * seams between pages, and the surrounding card blends those into the theme.
 */
.cv-embed{
  --accent: var(--global-base-color, #2f7f93);
  position: relative;
  width: 100%;
  height: 1100px;
  max-height: 88vh;
  padding: .55rem;
  border-radius: 14px;
  background: var(--global-card-bg-color, #fff);
  border: 1px solid color-mix(in srgb, var(--accent) 20%, transparent);
  box-shadow:
    0 1px 2px rgba(16, 24, 32, .04),
    0 12px 28px -12px color-mix(in srgb, var(--accent) 32%, transparent);
}
.cv-embed object,
.cv-embed iframe{
  display: block;
  width: 100%;
  height: 100%;
  border: 0;
  border-radius: 9px;
  background: var(--global-bg-color, #e7ebf0);
}
.cv-fallback{
  padding: 2rem;
  font-size: .95rem;
  line-height: 1.6;
}
/* Inline PDF viewers are unreliable on phones — show the buttons above instead. */
@media (max-width: 768px){
  .cv-embed{ display: none; }
}
</style>

<div class="cv-actions">
  <a href="{{ base_path }}/files/Academic_CV.pdf" target="_blank" rel="noopener">Open PDF in new tab</a>
  <a href="{{ base_path }}/files/Academic_CV.pdf" download>Download PDF</a>
</div>

<div class="cv-embed">
  <object data="{{ base_path }}/files/Academic_CV.pdf#toolbar=0&amp;navpanes=0&amp;statusbar=0&amp;view=FitH" type="application/pdf">
    <iframe src="{{ base_path }}/files/Academic_CV.pdf#toolbar=0&amp;navpanes=0&amp;statusbar=0&amp;view=FitH" title="Academic CV"></iframe>
    <p class="cv-fallback">
      Your browser cannot display PDFs inline.
      <a href="{{ base_path }}/files/Academic_CV.pdf">Download the CV (PDF)</a> instead.
    </p>
  </object>
</div>
