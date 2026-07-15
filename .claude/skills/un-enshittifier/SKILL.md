---
name: un-enshittifier
description: Strips LinkedIn and corporate thought-leadership posts down to what actually happened, deflating jargon and engagement bait into a short honest rewrite plus a funny one-liner. Use when the user pastes or describes a LinkedIn post, corporate announcement, or "thought leadership" text and wants it de-bloated, roasted, or translated to plain language.
---

# Un-enshittifier

## What this does

Takes a LinkedIn post, corporate announcement, or thought-leadership text and deflates it back to the real event underneath: what actually happened, said plainly, in the post's original language. The bloat  — jargon, epiphany arcs, hero numbers, engagement bait — gets stripped and, where interesting, called out.

## Output format (exactly this, in order)

1. **The bullshit meter** — grade how much of the post is bloat vs. substance, from 0% (a plain honest statement of fact) to 100% (pure engagement-farming with no underlying event at all). Lead with it so the verdict lands first: a bold label in the post's language ("Medidor de caca" for Spanish, "Shit-o-meter" for English), the 💩 emoji, the percentage in bold, then a 10-segment gauge bar in inline code, filled proportionally (█ per 10%, ▌ for a half step, ░ for the rest). No justification here — the rest of the output is the justification. Calibrate roughly: each tell from the catalog adds bloat; a post that still contains a real, verifiable event underneath caps around 80%; reserve 90%+ for posts where stripping the bloat leaves nothing.

   **Medidor de caca: 💩 80%** `[████████░░]`

2. **The rewrite** — a plain-language statement of what actually happened. 1–2 sentences, no drama, no jargon. MATCH THE ORIGINAL LANGUAGE of the post (Spanish post → Spanish output, English post → English output). Format it as a short quoted/offset block:

   > Partimos los squads grandes en grupitos de 3.

3. **The one-liner** — a single brutally honest, funny sentence capturing what the post is really *doing* (usually: someone did an ordinary thing and dressed it up as wisdom). **Bold it.**

4. **The tells** (only if genuinely interesting) — a short prose list of the manipulation tricks used, drawn from the catalog below. Skip this section entirely if the post is boringly honest.

## Hard rules

- The humor MUST come from deflation, NEVER from invention. Only mock what is literally on the page. Do NOT add facts, motives, or events the post does not state.
- Shorter is always better. If two words work, do not use ten.
- NEVER use the post's jargon unironically. "micro-células" becomes "grupitos". "synergy" becomes "working together". If you must quote the jargon, quote it to mock it.
- The ENTIRE output — rewrite, one-liner, and tells — MUST be in the original language of the post. No mixing: a Spanish post gets a fully Spanish output, including the tell names and section labels (e.g. "Las señales") and the meter label ("Medidor de caca" / "Shit-o-meter"); only the 💩, percentage, and gauge are language-neutral.
- Default tone: deflating but not cruel — an affectionate roast, not scorched earth. Only escalate if the user explicitly asks for it.

## Catalog of common tells (reference for step 4)

These are not inventions — each maps to a documented persuasion technique. The full grounded version, with the psychological mechanism and the research behind each tell, lives in [references/catalog.md](references/catalog.md). **Read that file and answer from it whenever the user asks why a tell works, whether this is "real", or wants to learn/teach the underlying techniques** — cite the actual sources, drop the roasting tone, keep it factual.

- **Borrowed authority** — name-dropping big companies (Google, Amazon, McKinsey) so you can't argue. (Appeal to authority; Cialdini's authority principle.)
- **Fake paradox** — "una paradoja que no vi venir"; framing an obvious consequence as a mind-bending contradiction. (Manufactured curiosity gap; pseudo-profundity.)
- **Personal-epiphany arc** — a mundane decision reframed as a revelation ("and that's when I realized…"). (Narrative transportation: stories suppress counterarguing.)
- **Bumper-sticker lesson** — "la lección: …"; the post exists to deliver a fortune cookie. (Processing fluency; unfalsifiable = information-free.)
- **Comment-farming question** — an open question bolted to the end to juice engagement ("¿A ustedes les ha pasado?"). (Engagement bait — formally defined and demoted by Meta since 2017.)
- **Buzzword bolted on for relevance** — AI, transformation, agile, sprinkled on unrelated content. (Trend-hijacking; jargon as status display.)
- **One-sentence-per-paragraph cadence-theater** — line breaks doing the work the ideas can't. (Fluency-as-truth, plus gaming the "see more" fold.)
- **Giant hero-number graphic** — a big "4x" in place of actual data or methodology. (Anchoring; denominator-free statistics.)
- **Preemptive defense** — "aquí no se trata de X" / "this isn't about layoffs" — the tell that X is exactly the fear. (Apophasis: denying a frame plants it.)

## Examples

### Example 1

**Input:** A post announcing the splitting of 4 big squads into 3-person "micro-células" because AI made devs faster and coordination became the bottleneck. Written as a personal journey with a paradox, a lesson, and a closing question.

**Output:**

**Medidor de caca: 💩 75%** `[███████▌░░]`

> Partimos los squads grandes en grupitos de 3. Los devs con IA tiran código más rápido de lo que podemos ponernos de acuerdo, así que ahora hay menos gente en cada reunión para no ponerse de acuerdo.

**"Reorganicé el equipo y escribí 8 párrafos para que suene como filosofía."**

Las señales: una paradoja falsa ("la paradoja que no vi venir"), un arco de epifanía personal sobre una reorganización rutinaria, una moraleja de galleta de la fortuna, y una pregunta al final para cosechar comentarios.

### Example 2

**Input:** A CEO post claiming "medimos un aumento de 4x en la productividad" with a giant "4x" graphic, several paragraphs explaining why the number is impressive, and zero explanation of how it was measured. Tagged "SERIE 2/6".

**Output:**

**Medidor de caca: 💩 90%** `[█████████░]`

> Medimos que los ingenieros van 4x más rápido con IA. No expliqué cómo lo medimos.

**"Tengo un número grande, un gráfico gigante que lo repite, y cero idea de cómo lo calculé."**

Las señales: todo el post defiende el número sin decir nunca cómo se midió; un gráfico gigante con el numerote como sustituto de datos; y "SERIE 2/6" — cosecha de calendario de contenidos, esto ya es una franquicia.
