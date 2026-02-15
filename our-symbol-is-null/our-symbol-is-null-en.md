---
layout: default
title: "The Symbol for All of Us is Null"
date: 2026-02-14
lang: en
key: our-symbol-is-null
tags: [mathematics, philosophy, machinelearning, beginners]
---

## **The Symbol for All of Us is Null**

You might be thinking, "What is this guy even talking about?"

But if you've found your way to this post, I have a feeling this will click for you somewhere along the way.

**Give me five minutes.**

- There's something humanity does unconsciously to make sense of the world.
- AI does the exact same thing.
- Mathematics describes it beautifully.

And at the end:

- **Why is Null the ultimate symbol for everything?**

It all connects in a single thread.

And once you see that thread, **the world starts to look a little clearer.**

Let's walk through it.

---

## To Understand Is to Divide

The world is full of things we don't understand.

But we have a trick for dealing with that: we give different things names and sort them into categories.

Round fruits? We split them into:

- Apples
- Oranges
- Pears

…and that's how we make sense of them.

This is the logic of cognition that every one of us runs unconsciously.

---

## AI Does the Same Thing

AI **understands words as vectors in absurdly high-dimensional space.**

What does that even mean? Let's--true to form--*divide and understand*:

- **Words:** assign IDs to things and concepts
- **Absurdly high-dimensional:** thousands or even tens of thousands of indices
- **Vectors:** array-format data you can think of as arrows with direction and magnitude
- **Understands:** tidies them up nicely

In pseudocode:

```
apple  = [2, 3, 5, ...]
orange = [3, 5, 7, ...]

dirOfApple = GetDirection(apple)
lenOfApple = GetLength(apple)
```

- In real LLMs, these vectors live in thousands or even tens of thousands of dimensions.  
  From a human perspective, the combinations are just… endless.

Visually, it looks something like this:

<object data="./assets/images/embedding.svg" type="image/svg+xml" style="max-width:50vw;"></object>

This is roughly how LLMs like ChatGPT and Gemini work under the hood--it's called **embedding**.

For a deeper dive, check out 3Blue1Brown's videos. Absolute masterpieces:

- [Transformers, the tech behind LLMs – Deep Learning Chapter 5](https://www.youtube.com/watch?v=wjZofJX0v4M)

---

## Analogy ↔︎ Contrast / Induction ↔︎ Deduction / Concrete ↔︎ Abstract

Most sports and martial arts have fundamental forms. So does the way we see and think about things.

These three pairs are the basic stances of reasoning. Most people use them without realizing it. But once you name and practice them consciously, you'll understand *anything* faster and deeper.

<pre>
Analogy ↔︎ Contrast :  
      Apples and oranges are both sweet.
                        ↑↓
      Apples are red; oranges are yellow.

Induction ↔︎ Deduction:  
      An apple fell from the tree. There seems to be gravity.
                        ↑↓
      An orange detached from a branch will fall due to gravity.

Concrete ↔︎ Abstract :  
      There's a round, red, sweet apple and a round, yellow, sweet orange.
                        ↑↓
      There are two round fruits.
</pre>


"Obvious?" Okay, let me explain a bit more carefully.
It's going to get gradually more serious from here.
We'll use some light math, but nothing super rigorous, 
so take it easy. Skipping the formulas is totally fine.

---

### Analogy and Contrast Are Mappings

Analogy is finding what's the same. Contrast is finding what's different.

An example:

An apple is round, red, and sweet.  
An orange is round, orange, and sweet.

Apply analogy and contrast:

<pre>
Analogy: a linear transformation toward the same direction  
                     → Apples and oranges are both sweet and round  
          
Contrast: a linear transformation toward opposite directions 
                     → Apples are red, but oranges are orange
</pre>


As a vector diagram:

<object data="./assets/images/analogy-and-contrast.svg" type="image/svg+xml" style="max-width:90vw;"></object>

In notation, using linear maps $ T_{analogy} $ and $ T_{contrast} $:

- $ \text{Analogy} : T_{analogy}(\vec{apple}) \uparrow T_{analogy}(\vec{orange}) $

- $ \text{Contrast} : T_{contrast}(\vec{apple}) \downarrow T_{contrast}(\vec{orange}) $

---

### Induction and Deduction Are Vector Subtraction and Addition

Induction is searching for laws from specific past observations.  
Deduction is inferring specific future events from laws.

Newton's universal gravitation is the classic example.

<pre>
Induction:  Extracting a law vector  
  → An apple fell from the tree. There seems to be gravity.

Deduction:  Superposing a law vector  
  → An orange detached from a branch will fall to the ground due to gravity.
</pre>

As a vector diagram:

<object data="./assets/images/induction-and-deduction.svg" type="image/svg+xml" style="max-width:90vw;"></object>

In notation:

- $ \text{Induction} : \text{Extraction}(\vec{fact_1}, \vec{fact_2}, \dots) \Rightarrow \vec{law} \mid \vec{law} = \vec{facts} - \frac{\sum \vec{noise}}{n} $

- $ \text{Deduction} : \text{Superposition}(\vec{object}) \Rightarrow \vec{future} \mid \vec{future} = \vec{object} + \vec{law} $

- Induction is *estimation*.  
  You stack multiple observations, cancel out the noise, and let the hidden law float to the surface.   
- Deduction is *certainty*.  
  A law applies to the future, no ifs or buts.

---

### Concrete and Abstract Are Gain and Loss of Information

- **To concretize** is to add parameters (attributes), increasing information,   
  no special rules.
- **To abstract** is to remove parameters (attributes), reducing information  
  **toward the nice essence.**  

An example:

Take the abstraction "fruit." Add the parameters "round," "red," and "sweet," and you get "apple."  
Take "apple" and strip away various parameters, and you might end up with just "round."

As a diagram:

<object data="./assets/images/concretize-and-abstract.svg" type="image/svg+xml" style="max-width:90vw;"></object>

In notation:

- $ \text{Concretize}(\vec{object}) \Rightarrow \vec{object} \oplus \vec{parameters} $

- $ \text{Abstract}(\vec{object}) \Rightarrow \vec{object} \ominus \vec{parameters} $

Take the abstraction "human." Add the parameters "47 years old" and "male,"  
and you get "middle-aged dude." 🍺

---

## The Nice Essence

When you abstract by stripping away information, doing it haphazardly leads to nonsense.  
Remove the stubble and wrinkles from a middle-aged man and you just get a boy.  
That's not what we want--want to extract the information that actually matters.

That's where **PCA (Principal Component Analysis)** comes in.  

PCA? Sounds fancy? You've probably already experienced it though.

You know those personality quizzes with ~50 questions that plot you on a matrix like "Instinctive ↔ Logical" vs. "Extroverted ↔ Introverted"?  
Those 50 questions are basically a 50-dimensional vector.  
PCA squishes it down to 2 dimensions to make a "personality map."

<object data="./assets/images/personality_profiling_ja.svg" type="image/svg+xml" style="max-width:90vw;"></object>

In notation:

- Extraction:
  $\text{Extract}(\vec{data}) \Rightarrow \vec{essence} \mid \vec{essence} = Z W_k \mid W_k = [\vec{v}_1, \dots, \vec{v}_k] \text{ where } \Sigma \vec{v} = \lambda \vec{v}$

  - $ Z$: Zero-centering
  - $ W$: Weight matrix
  - $ \lambda$: Eigenvalues = the size of each MECE-organized component of information
  - MECE: Mutually Exclusive, Collectively Exhaustive

Set $ k = 2 $ and you get a 2D matrix.

This is pretty much the same thing we do unconsciously when we "get the gist" of something.

For more, this video is excellent:

- [Abstract vector spaces – Chapter 16, Essence of Linear Algebra](https://www.youtube.com/watch?v=TgKwz5Ikpc8)

---

### A Symbol Is the First Principal Component

When you organize information about something, some of it matters more than the rest. Naturally, you want to express the most important piece as simply and memorably as possible.

That's what **symbols** are.  

Flags, logos, kings, pop idols…

When people rally around a symbol, here's what they're actually doing: from everyone's messy, sprawling vectors, they're zeroing in on the single most important one.

That most important vector = PCA's **first principal component**.

<object data="./assets/images/symbol.svg" type="image/svg+xml" style="max-width:90vw;"></object>

The first principal component of PCA is "the direction of maximum variance"--the vector that preserves the most information about the group. The arrow that best represents everyone.  
In other words: **symbol**.

---

### What's at the End of Abstraction?

Abstraction strips away information toward the **nice essence**.

- Strip a solid down and you get a plane.
- Strip a plane down and you get a line.
- Strip a line down and you get a point.  
  → $ \mathbb{R}^0 $ still contains the information "a single point exists."
- Strip even that away, and…?

$$
\mathbb{R}^3 \to \mathbb{R}^2 \to \mathbb{R}^1 \to \mathbb{R}^0 = \{*\} \to \emptyset = \text{Null}
$$

What remains is **empty space.**

## That Is **Null**.

<object data="./assets/images/ultimate-symbol.svg" type="image/svg+xml" style="max-width:90vw;"></object>

If you keep abstracting everything in the universe, you arrive at **Null**--**nothingness**.

And so **Null**:

- Belongs to no one.
- Carries no attributes.
- Is the **ultimate symbol**, with every vector stripped away.

Apples, oranges, you, me -- all of us.

### Strip away the infinite-dimensional noise, and everyone arrives at the same space. That space is **Null.**

The primordial void before creation. *Form is emptiness.* The Big Bang. They're all pointing at the same thing.

#### Friends who share the same symbol -- let's get along! ✌️

---

(c) 2026 GoodRelax. MIT License.
