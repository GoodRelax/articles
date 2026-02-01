---
layout: default
title: "Read UML Class Diagrams as Sentences"
date: 2026-02-01
lang: en
key:  class_diagram_01
tags: [uml, class-diagram, design, dip]
---

## Index
* Table of Contents
{:toc}

---

# Read UML Class Diagrams as Sentences

UML has been around for a long time, and among all UML diagrams, the **class diagram** is probably the one that still survives in real-world development.

And yet, every time we read or draw one, we get stuck on the same things:

* What does this arrow mean again?
* Which direction is correct?
* How should I read “dependency”, “association”, and “aggregation”?

I don’t think this confusion comes from a lack of UML knowledge.

The real problem is that **we don’t share a rule for how to read a class diagram**.

So I made a cheat sheet to fix that.

This cheat sheet:

* Covers all arrows used in UML class diagrams
* Defines a simple template to “read arrows as sentences”
* Reduces confusion when reading and writing class diagrams

---

## The Cheat Sheet

**Cheat sheet:**
[https://goodrelax.github.io/gr-cheat-sheets/uml/class-diagram-cheat-sheet-en.html](https://goodrelax.github.io/gr-cheat-sheets/uml/class-diagram-cheat-sheet-en.html)

It summarizes every arrow used in UML class diagrams and how to read them.

I also added sample code in C++, JavaScript, and Python to show how each relationship appears in actual code.

---

## The Key Idea: Read Arrows as Sentences

For every arrow, read it using this template:

> **Subject (start) + Verb (arrow type) + Target (end)**
> 
> The “target” can be either an object or a complement depending on the relationship.
 
That’s it.

By doing this, a class diagram stops being a “picture” and becomes **a set of readable sentences**.

Two rules matter:

1. The **start of the arrow is always the subject**
2. Choose a **verb that matches the arrow type and direction**

Once this rule is shared, misreading class diagrams almost disappears.

---

## Why This Works So Well

### Faster Reviews

You can instantly verbalize what the diagram means.

### Easier to Spot Design Mistakes

When you turn it into a sentence, awkward designs become obvious.

For example:

> “PaymentData refers to Repository”

If you can read it like this, you immediately feel something is wrong.

### Easier to Check DIP (Dependency Inversion Principle)

Because you can read dependencies as sentences, it becomes much easier to see where the design intent is broken.

---

## Do We Still Need Class Diagrams in the Age of AI Coding?

AI is getting better at coding.

We are heading toward a world where:

* Humans do high-level thinking
* AI designs
* Other AIs implement and test

Even then, humans will still be responsible for:

* Reviewing designs
* Monitoring structure
* Checking dependencies

At that point, the ability to **read class diagrams as sentences** becomes even more important.

---

## Conclusion

Understanding class diagrams is not about UML knowledge.

It’s about having **a rule for how to read them**.

I hope this template helps reduce the time you spend being confused by class diagram arrows.

---

## Cheat Sheet Preview

Here are the most commonly used parts of the cheat sheet.

For full details and sample code, see:
[https://goodrelax.github.io/gr-cheat-sheets/uml/class-diagram-cheat-sheet-en.html](https://goodrelax.github.io/gr-cheat-sheets/uml/class-diagram-cheat-sheet-en.html)

![Class Diagram Cheat Sheet](https://goodrelax.github.io/gr-cheat-sheets/uml/class_diagram_cheat_sheet_en.png)
![Class Diagram Cheat Sheet Description Table](https://goodrelax.github.io/gr-cheat-sheets/uml/class_diagram_cheat_sheet_table_en.png)
