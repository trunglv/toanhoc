---
title: "Euler's identity, explained in one line"
date: 2026-11-08 09:00:00 +0700
categories: [dai-so]
lang: en
---

<div class="math-block">
$$e^{i\pi} + 1 = 0$$
</div>

It links five constants that come from different corners of mathematics: $e$ from growth, $i$ from imaginary numbers, $\pi$ from circles, $1$ and $0$ from counting. The reason it holds is simpler than it looks.

## The key formula

Define $e^{ix}$ by its power series, the same way you would define $e^x$:

<div class="math-block">
$$e^{x} = 1 + x + \frac{x^2}{2!} + \frac{x^3}{3!} + \cdots$$
</div>

Substitute $ix$ and separate the real and imaginary parts, using $i^2 = -1$. The even powers give the series of $\cos x$, and the odd powers give the series of $\sin x$:

<div class="math-block">
$$e^{ix} = \cos x + i\sin x$$
</div>

This is Euler's formula. It describes a point moving around the unit circle as $x$ grows.

## Plug in $x = \pi$

<div class="math-block">
$$e^{i\pi} = \cos \pi + i\sin \pi = -1 + 0 \cdot i = -1$$
</div>

Move the $-1$ across the equals sign and you get $e^{i\pi} + 1 = 0$.

<div class="note">
<span class="note-label">Why it matters</span>
<p>Walking half a turn around the unit circle lands you at $-1$. Exponential growth and rotation turn out to be the same process, seen from two sides.</p>
</div>
