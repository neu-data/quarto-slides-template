<div align="center">

<img src="https://raw.githubusercontent.com/neu-data/.github/main/assets/banner.svg" alt="Neudata Consulting Ltd" width="100%" />

# Neudata Quarto slides

**Web-based presentations with live code output — matching the Neudata PowerPoint and Beamer templates.**

![Quarto](https://img.shields.io/badge/Quarto-revealjs-055F56?style=flat&logo=quarto&logoColor=white)
![Neudata](https://img.shields.io/badge/Neudata-brand-04242F?style=flat)

</div>

---

Download [`examples/example-slides.html`](examples/example-slides.html) and open it in a browser to see every slide type (it is self-contained).

## What you get

| Slide | How |
|---|---|
| **Title slide** — centred teal title, presenter, large logo bottom-left, date bottom-right | Front matter (`title`, `subtitle`, `author`, `institute`, `date`) |
| **Section divider** — logo, teal rule, section name and number | `# Section name` |
| **Content slide** — teal title with rule, small logo, `Neudata \| #ClearDataClearImpact`, slide number | `## Slide title` |
| **Blue notes** (as in the PowerPoint *Title and Notes* layout) | `[Notes]{.neudata-note}` |
| **Big-number callouts** | `[87.4%]{.neudata-stat}` + `[coverage]{.neudata-stat-label}` |
| **Key-findings box** | `::: {.key-findings}` |
| **Live R / Python code** with output beside it | `#| output-location: column` |
| **Branded tables** — navy header, striped rows | Markdown tables or `knitr::kable()` |
| **Closing copyright slide** | Added automatically; `copyright-slide: false` to remove |

## Start a new deck

```bash
quarto use template neu-data/quarto-slides-template
```

Or add the format to an existing project:

```bash
quarto add neu-data/quarto-slides-template
```

Then render and present:

```bash
quarto preview talk.qmd
```

Keyboard: **F** full screen · **S** speaker notes · **O** slide overview · **E** print view (save as PDF from the browser).

## Front matter

```yaml
---
title: "Presentation Title"
subtitle: "Optional subtitle"
author: "Presenter Name, Role"
institute: "Neudata Consulting Ltd"
date: today
date-format: "DD-MM-YYYY"
format: neudata-revealjs
---
```

## Share a single file

```bash
quarto render talk.qmd -M embed-resources:true
```

produces one self-contained `.html` you can email or upload.

## Fonts and colours

Century Gothic (as in the PowerPoint template) where installed, with close fallbacks. Teal `#0D7377` titles, blue `#0070C0` notes, navy `#04242F`, logo teal `#055F56`, mist `#EAF2F5`.

---

<div align="center">

**Neudata Consulting Ltd** · *Insight. Impact. Innovation.*
[www.neu-data.com](https://www.neu-data.com) · [contact@neu-data.com](mailto:contact@neu-data.com)

</div>
