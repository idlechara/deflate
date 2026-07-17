# balloon 💩

**A Claude Code plugin that un-enshittifies LinkedIn posts.**

Paste any thought-leadership post, corporate announcement, or "personal journey" homily, and get back the real event underneath — said plainly, in the post's own language — plus a bullshit meter, a brutally honest one-liner, and a breakdown of the manipulation tricks used.

## Example

Feed it a (fully invented) post where a founder announces "redujimos el tiempo de onboarding 10x" over a giant 10x graphic, with zero methodology, tagged "parte 3/7":

> **Medidor de caca: 💩 90%** `[█████████░]`
>
> > Decimos que nuestro onboarding es 10x más rápido. No expliqué comparado con qué ni cómo lo medimos.
>
> **"Tengo un número grande, un gráfico gigante que lo repite, y cero idea de cómo lo calculé."**
>
> Las señales: todo el post defiende el número sin decir nunca cómo se midió; un gráfico gigante con el numerote como sustituto de datos; y "parte 3/7" — cosecha de calendario de contenidos, esto ya es una franquicia.

(All examples in this repo are invented specimens of the genre — any resemblance to an actual post is the genre's fault, not ours.)

## Install

In Claude Code:

```
/plugin marketplace add idlechara/balloon
/plugin install balloon@balloon
```

## Use

```
/balloon:deflate <paste the post>
```

Screenshots work too — paste an image of the post.

Or run it in reverse:

```
/balloon:inflate <a plain, boring fact>
```

**Inflate** takes a fact and inflates it into full thought-leadership glory — epiphany arc, fake paradox, fortune-cookie lesson, comment-farming question — using the exact same catalog of tells as a recipe instead of a detector. It never invents facts: every gram of added weight is content-free drama, which is the joke. Ask for a bloat level ("mild", "90%", "maximum slop"); default is 75%. The output should survive a round-trip through /balloon:deflate and come back as exactly your fact.

## What you get

1. **The bullshit meter** — 0% (a plain honest fact) to 100% (pure engagement farming with nothing underneath), with a gauge bar. Posts with a real event under the bloat cap around 80%; 90%+ is reserved for posts where stripping the bloat leaves nothing.
2. **The rewrite** — what actually happened, in 1–2 sentences, in the post's original language.
3. **The one-liner** — what the post is really *doing*, in one sentence.
4. **The tells** — the manipulation techniques at work, when they're interesting.

## The serious part

The humor comes strictly from deflation, never invention — the skill only mocks what is literally on the page. And the "tells" aren't made up either: each one maps to a documented persuasion technique — appeal to authority (Cialdini), pseudo-profound bullshit (Pennycook et al., 2015), narrative transportation (Green & Brock, 2000), processing fluency, anchoring (Tversky & Kahneman, 1974), engagement bait (formally defined and demoted by Meta since 2017), and classical apophasis.

The full grounded catalog — mechanism, research, and a practical "how to spot it" test for each tell — lives in [skills/deflate/references/catalog.md](skills/deflate/references/catalog.md). Ask the skill *why* a tell works and it answers from there, sources included, roast off. The framing owes everything to Harry Frankfurt's *On Bullshit*: these posts usually aren't lies — they're indifferent to truth, optimized for effect. That's what makes them deflatable.

## License

MIT
