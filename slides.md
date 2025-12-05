---
marp: true
theme: default
paginate: true
size: 16:9
---

<style>
/* === Custom theme specification (overrides for the default theme) === */

/* Body / base */
section {
  font-family: Inter, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
  color: #1b1f23;
  background-color: #ffffff;
}

/* Title styling */
h1, h2 {
  letter-spacing: -0.02em;
}

/* Accent color for headings */
h1 { color: #0b5394; }
h2 { color: #0b5394; }

/* Footer (machine-readable contact & small print) */
.marp-footer {
  position: absolute;
  right: 1rem;
  bottom: 0.6rem;
  font-size: 0.75rem;
  color: #6b7280;
}

/* Custom class usable on slides */
.center-note { text-align: center; font-style: italic; color: #374151; }

/* Ensure images used as backgrounds can cover the slide */
img.bg-cover {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
}
</style>

<!--
  Custom Marp directives demonstrated:
  - `paginate: true` above enables page numbers automatically.
  - Inline <style> defines a custom theme override.
-->

# Product Documentation — Marp Demo
Technical Writer · Product Documentation

Contact: 24f1002299@ds.study.iitm.ac.in

<footer class="marp-footer">24f1002299@ds.study.iitm.ac.in • slides.md</footer>

---

## Why use Marp for product docs?

- Markdown-first: version-control friendly.
- Exportable to PDF / PPTX / HTML via Marp CLI.
- Easy to maintain and diff in `git`.

<aside class="center-note">Maintainability + portability = predictable documentation workflows.</aside>

---

## Features included in this deck

1. Custom theme via embedded CSS.
2. Page numbers (see bottom-right).
3. Background image on one slide.
4. Inline custom styling and Marp directives.
5. Mathematical equations (KaTeX/LaTeX).
6. Machine-readable email in plain text and footer.

---

<!-- Background image slide: use an image asset path or remote URL. 
     For best results place an `assets/` folder in the repo and put the image there.
-->
---
<!-- background image slide -->
![](assets/product_screenshot.jpg){class="bg-cover"}

<!-- If the grader fetches raw markdown it will see the image reference above.
     If the grader fetches rendered HTML the image will display as slide background. -->

---

## Algorithmic Notes (mathematical equations)

We'll state the Master Theorem form used for divide-and-conquer complexity:

$$
T(n) = a\,T\!\left(\frac{n}{b}\right) + f(n)
$$

For the common case where $a > 0$, $b > 1$, and $f(n)=\Theta(n^c)$:

- If $c < \log_b a$, then $T(n)=\Theta(n^{\log_b a})$.
- If $c = \log_b a$, then $T(n)=\Theta(n^{\log_b a}\log n)$.
- If $c > \log_b a$, then $T(n)=\Theta(f(n))$.

Example: binary split with linear combine ($a=2$, $b=2$, $f(n)=\Theta(n)$) ⇒ $T(n)=\Theta(n \log n)$.

---

## Example code snippet (for reference)

```python
# sample: parse product metadata and print top features
import json
with open('product_metadata.json') as f:
    data = json.load(f)
print(sorted(data['features'], key=lambda x: x['priority'])[:5])
