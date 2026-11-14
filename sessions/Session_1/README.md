# Session 1: Understanding deep learning requires rethinking generalization

- **Paper:** [Understanding deep learning requires rethinking generalization (Zhang et al., ICLR 2017)](https://arxiv.org/abs/1611.03530)
- **Date:** Friday, 13 November 2026
- **Session leads:** Bilal and Husnain

## Main claim

We do not know why deep learning models generalize. Many people believe two things that when a model has more parameters than data, it does not generalize and regularization makes it generalize. This paper shows that neither belief explains why generalization happens.

## Critique

- The authors strongly argue against the existing beliefs. But Sections 4 and 5 do not explain generalization from a deep learning perspective. Both sections solve a linear system, like the normal equation, without backpropagation.

## Members' notes

Each member adds their own notes file in this folder: `<YourName>_SESSION_1_notes.md`.

## Connection to our question

The paper removes two common explanations (model capacity and regularization). It does not give a new explanation. It leaves our question open on how the same model fits true labels and random labels, but only the true labels generalize.

## Open questions

- A model can learn random labels and true labels. With true labels it generalizes, with random labels it does not. What makes sure that it generalizes?
- Humans can remember phone numbers. A phone number has no meaning, so we memorize it, but we do not generalize from it. Is generalization the same as finding a rule that we can apply anywhere (maybe compression)? Is memorization what remains when there is no rule?
- Ilya Sutskever says that generalization happens through compression. This is a popular belief, but nobody knows exactly. We can study it more.
