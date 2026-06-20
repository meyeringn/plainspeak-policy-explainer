# PlainSpeak Policy Explainer

**A free, browser-only tool that scores public policy text for reading level, flags bureaucratic jargon, and drafts a plain-language rewrite — then shows you exactly how many grade levels of difficulty it removed.**

🔗 **Live tool:** https://meyeringn.github.io/plainspeak-policy-explainer/

![No backend](https://img.shields.io/badge/backend-none-1C5C54)
![Privacy](https://img.shields.io/badge/data-never%20leaves%20your%20browser-1C5C54)
![Accessibility](https://img.shields.io/badge/built%20for-screen%20readers%20%26%20dyslexia-1C5C54)
![License](https://img.shields.io/badge/license-MIT-blue)

---

## Why this exists

Most U.S. adults read most comfortably at about a 7th-to-8th-grade level. A lot of government writing lands several grades above that — which means the people a notice is legally meant to inform are the ones most likely to skim it, misread it, or give up.

That gap isn't a literacy failure on the reader's side. It's a design failure on the institution's side. It hits hardest for Disabled people, people with cognitive disabilities, and people reading in a second language — the exact communities public policy most often affects.

PlainSpeak treats clear writing as a civic access issue, not a style preference. Paste a dense ordinance, public notice, or policy and the tool does three things: it scores how hard the text is to read, highlights the jargon, and drafts a plainer first version — so you can see the problem *and* a path out of it.

## What it does

- **Scores the reading level** using the Flesch–Kincaid grade-level formula and the Flesch Reading Ease score.
- **Flags bureaucratic jargon** against a curated plain-language dictionary, with the everyday swap shown for each term.
- **Drafts a plain-language first version** entirely with rules — no AI call, nothing uploaded.
- **Shows the before/after grade drop** on an animated reading-grade meter, with the difficulty difference stated in plain numbers.
- **Translates the score into stakes** — turning a grade number into a sentence about who gets left out.

Everything runs in your browser. Your text never leaves the page.

## Built to be read every way

The tool is also a small demonstration of the accessibility it argues for. It includes:

- A **dyslexia-friendly font** toggle (OpenDyslexic, with a legible fallback).
- A **high-contrast** mode.
- **Text-size** controls.
- A skip link, semantic landmarks, and a clear heading order.
- **Screen-reader announcements** — results are read aloud through a live region when analysis finishes.
- Jargon flagged with an **underline and a label**, never by color alone.
- Visible keyboard focus, and reduced motion respected for anyone who prefers it.

## How to use it

1. Open the [live tool](https://meyeringn.github.io/plainspeak-policy-explainer/).
2. Paste any policy text — or click **Load example notice** to see it work.
3. Click **Analyze the writing**.
4. Read the grade drop, scan the flagged jargon, and copy the plain-language draft.

Always have a person check the rewrite before using it. The draft is a starting point, not a final answer.

## How it scores

Short version: reading grade uses **Flesch–Kincaid Grade Level**; ease uses the **Flesch Reading Ease** score; jargon and rewrites come from a curated rule set. The full math, the rewrite pipeline, and an honest list of limitations are documented in **[METHODOLOGY.md](METHODOLOGY.md)**.

## Tech

A single `index.html`. No build step, no dependencies to install, no API keys, no server. Hosted on GitHub Pages. Fork it, change the jargon dictionary in the script, and you have a plain-language tool tuned for your own city or agency.

## Part of a civic tech portfolio

PlainSpeak sits alongside other browser-only tools built on the idea that transit equity, disability justice, and climate action are one connected fight — including CanopyWatch, FloodRisk Philly, the Transit Carbon Calculator, the Climate Civic Action Advisor, and the Climate Equity Policy Simulator. See them all at **[github.com/meyeringn](https://github.com/meyeringn)**.

## License

MIT. Use it, fork it, build on it. Clear public writing should belong to everyone.

---

*Built in Philadelphia. 🧡🖤*
