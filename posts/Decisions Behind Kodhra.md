# Design Decisions Behind Kodhra

When I started building **Kodhra**, I wasn’t trying to create “another code snippet manager”. That already exists. Plenty of them.
What I wanted was something simpler, faster, and closer to how *I actually think while coding*.

This post is not about features. It’s about **why certain decisions were made**, what I avoided, and what I learned in the process.

---

## 1. The Problem Was Not “Storing Snippets”

Storing snippets is easy.

You can:

* dump them in JSON
* throw them in localStorage
* save them in a database

That’s not the hard part.

The real problem I personally faced was this:

> I remembered *that I had solved something before*, but I couldn’t remember **where**, **how**, or **why** I solved it that way.

Most snippet managers treat snippets like static text.
But real code is **contextual**.

* Why did I write this?
* What problem was I solving?
* What constraints existed at that time?

So from day one, Kodhra was designed around **context**, not just code.

---

## 2. Why I Didn’t Start With Features

A lot of projects fail because they start like this:

> “Let’s add tags, folders, sync, sharing, AI…”

I did the opposite.

I asked:

* How do *I* search my brain for old code?
* What words do I type when I’m stuck?
* Do I think in “folders” or in “problems”?

Answer: **problems**.

So Kodhra’s core idea became:

> “Snippets should be retrievable the same way you remember them.”

That influenced everything else.

---

## 3. Search First, UI Second

Most apps design UI first, then add search.

I flipped it.

Search was treated as the **main interface**, not a feature.

Because in real life:

* I don’t browse snippets
* I don’t scroll categories
* I **search**

That meant:

* search had to be fast
* forgiving
* usable even with vague keywords

If search fails, the whole app fails.
Everything else is secondary.

---

## 4. Why I Avoided Over-Engineering Early

I could have:

* added complex indexing
* built advanced ranking algorithms
* abstracted everything into layers

I didn’t.

Early over-engineering gives you:

* fake progress
* real complexity
* zero feedback

Instead, I followed a boring but effective rule:

> Build the simplest thing that reveals the next real problem.

Only after using Kodhra myself did new requirements appear naturally.

This saved time and mental energy.

---

## 5. Monorepo Was a Conscious Choice

I chose a monorepo not because it’s trendy, but because:

* frontend and backend evolve together
* shared types and utilities matter
* refactoring across boundaries is easier

For a tool like Kodhra, separation without coordination would slow me down.

Monorepo wasn’t about scale.
It was about **clarity**.

---

## 6. What I Intentionally Did NOT Add

This part matters.

I did **not** add:

* social features
* public snippet sharing
* unnecessary customization
* “AI for the sake of AI”

Why?

Because Kodhra is a **personal engineering tool**, not a social platform.

Every feature added has a maintenance cost.
I wanted something I could trust for years, not babysit forever.

---

## 7. The Biggest Lesson So Far

The biggest lesson wasn’t technical.

It was this:

> Tools should adapt to how developers think, not force developers to adapt to tools.

Once I internalized that, many decisions became obvious.

---

## 8. Kodhra Is Still Evolving (And That’s Fine)

Kodhra is not “finished”.
It probably never will be.

And that’s okay.

It’s growing based on **real usage**, not hypothetical users.

Every design decision so far has come from:

* frustration
* reflection
* and practical need

That’s the only kind of evolution I trust.

---

## Closing Thought

Kodhra is not my biggest project.
But it is one of the most **honest** ones.

It reflects how I think about:

* code
* tools
* and long-term engineering

And for me, that matters more than flashy features.
