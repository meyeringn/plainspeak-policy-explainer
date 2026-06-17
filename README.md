# PlainSpeak Policy Explainer

A free, browser-only tool that scores any policy, ordinance, or public notice for reading level, flags common bureaucratic jargon, and generates a plain-language first draft — all in real time, with nothing uploaded anywhere.

**Live demo:**  `https://meyeringn.github.io/plainspeak-policy-explainer/`_

## Why this exists

Plain language is a governance and access issue, not a style preference. When public notices, ordinances, and policy memos are written above the reading level of the people they govern, that's a quiet barrier to civic participation — the same way a broken curb cut is a barrier, just less visible. PlainSpeak gives any civic leader, city department, or community group a fast, honest gut-check on whether their public-facing writing is actually reaching the public.

This is part of an ongoing series of small, free civic tech tools — see [github.com/meyeringn](https://github.com/meyeringn) for the others.

## What it does

1. **Paste text** — an ordinance, notice, memo, anything.
2. **Get a reading-level score** — Flesch-Kincaid Grade Level and Flesch Reading Ease, plus word/sentence counts and a complex-word percentage.
3. **See the jargon** — terms matched against a curated glossary of common bureaucratic/legal language, each with a plain-language alternative.
4. **Get a draft rewrite** — jargon swapped out and some long sentences split, as an editable starting point.
5. **Share the result** — "Copy shareable link" encodes the text into the URL itself (in the hash, so it never touches a server) — open the link and the same analysis reproduces instantly.
6. **Print a clean report** — "Print report" strips out all the buttons and input controls and formats a one-page-style readout (scores, jargon list, full rewrite, methodology) suitable for attaching to testimony, a memo, or an email.

## Methodology and sources (read this before you trust the numbers)

Being upfront about how this works matters more than the tool looking polished:

- **Readability formulas:** Flesch-Kincaid Grade Level and Flesch Reading Ease are standard, public readability formulas dating to Rudolf Flesch's original work and J. Peter Kincaid's later adaptation. They estimate reading difficulty from sentence length and syllables per word — they don't understand meaning, tone, or context.
- **Syllable counting** uses a common heuristic (counting vowel groups), so scores are close approximations, not exact.
- **The jargon glossary** (in `index.html`, the `JARGON` object) is a manually curated list of roughly 50 common bureaucratic and legal terms, built from general plain-language writing guidance in the spirit of resources like plainlanguage.gov. It is illustrative, not exhaustive, and not an official or government-endorsed list. Pull requests adding terms are welcome.
- **The plain-language draft** is mechanical: glossary word-swaps plus splitting some long sentences. It will sometimes read awkwardly (e.g., grammar doesn't always survive a word swap cleanly). It's a first-pass drafting aid for a human editor — not a certified or finished plain-language document, and not legal advice.
- **WCAG context:** the Web Content Accessibility Guidelines include a Reading Level success criterion recommending public-facing text not require reading ability beyond a lower-secondary-education level unless an easier-to-read version is also offered. This tool helps writers see how far a draft is from that target. It does not determine legal or accessibility compliance on its own.

## Privacy

There is no backend, no analytics, no cookies, and no account. Every calculation happens in the browser's JavaScript. Nothing you paste is ever sent anywhere — you can confirm this by reading the single `index.html` file; there are no network calls in the code except loading two Google Fonts. The shareable-link feature encodes text into the URL fragment (after the `#`), which browsers never send to a server, so this stays true even when sharing.

## Deploying this yourself

No build step. To put this on GitHub Pages:

1. Create a new repo (or use this one) and add `index.html` to the root.
2. Go to **Settings → Pages**, set the source to the `main` branch, root folder.
3. Your live tool will be at `https://<your-username>.github.io/<repo-name>/`.

That's it — it's a single static HTML file.

## Limitations / honest caveats

- The jargon glossary is small and English-only; it won't catch every dense phrase, and it may occasionally flag a term that's actually fine in context.
- The syllable-counting heuristic can misjudge unusual or technical words.
- The rewrite is a draft, not a finished product — always have a person review it before it goes public.
- This tool measures *reading difficulty*, not clarity, accuracy, or whether the underlying policy itself is fair or sound. Those still require human judgment.
- Very long pasted documents will produce a very long shareable link. Most modern browsers handle this fine, but extremely long links can behave unreliably in some messaging apps.

## Credit

Built by Nico Meyering with Claude (Anthropic), as part of an ongoing civic tech project series exploring how small, free tools can support transparency and access in local government.

## License

MIT — use it, fork it, adapt the glossary for your own city or organization.
