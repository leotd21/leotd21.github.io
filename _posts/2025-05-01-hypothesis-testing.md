---
layout: post
comments: true
title: "Is My Coffee Getting Weaker?"
date: 2025-05-01
categories: [Stories]
tags: [hypothesis testing, statistics]
mathjax: false
---

<style>
p {
  text-align: justify;
}
.post pre, .post code {
    border: none;
    background-color: #eee;
}

</style>

---

The first sip of my usual latte didn’t hit the same today... and it wasn’t just my imagination. Right?

## The Latte Dilemma

You go to **Java Junction** every morning and order the same drink: a double-shot vanilla oat milk latte. Over the past week, something feels... off.

You suspect they’ve secretly **reduced the caffeine** content — maybe to cut costs?

Now you’re faced with the big question:

**"Is my coffee actually weaker, or am I just overthinking it?"**

Let’s use **hypothesis testing** to find out.

## What Is Hypothesis Testing?

Hypothesis testing helps us use **data** to answer yes/no questions like:

- "Is this new medication effective?"
- "Has customer behavior changed?"
- "Is my latte less caffeinated?"

It’s like a **courtroom trial**:  
You assume the shop is innocent (i.e., nothing changed) unless the **evidence** says otherwise.

## Setting Up the Hypotheses

Here’s what we test:

| Term                     | Meaning |
|--------------------------|---------|
| **Null Hypothesis (H₀)**      | The latte still has the usual caffeine (say, 150mg). |
| **Alternative Hypothesis (H₁)** | The caffeine content is **less** than 150mg.         |

This is a **one-tailed test** — we’re only worried if it’s **weaker**.

## The Evidence: You Collect Data

You bring a home caffeine tester (yes, they exist) and measure your latte for 7 days:

```
[142mg, 144mg, 143mg, 141mg, 140mg, 143mg, 142mg]
```

- **Sample mean** = 142.1mg  
- **Assumed population mean** = 150mg  
- **Sample size** = 7  
- **Estimated standard deviation** ≈ 1.3mg

## Running the Test

You decide on a significance level **α = 0.05** (5% chance you’re wrong if you reject H₀).

Using a **t-test** (small sample, unknown population std), you compute:

- **t-statistic** = (142.1 - 150) / (1.3 / sqrt(7)) ≈ -14.8  
- **p-value** ≈ 0.00001 (very small!)

## What Is a p-value, Really?

The **p-value** tells you how likely you are to see a sample like yours (or more extreme) **if the null hypothesis were true**.

In our case:  
If your lattes really still had 150mg of caffeine, how likely is it to measure an average of 142.1mg or less, just due to random variation?

A **small p-value** means:  
"Whoa, this result is too unlikely under the null — maybe the null isn't true."

In plain English:  
If the coffee *were* still 150mg, the odds of randomly getting your weak-tasting results are extremely low. So it's reasonable to believe something **has changed**.

## Decision Time

Since **p < 0.05**, you **reject the null hypothesis**.

**Conclusion:** Your coffee **is** weaker — statistically speaking.

## Why This Matters

This may seem like a coffee problem, but the concept powers much of modern science and business:

- A/B testing websites
- Drug trial approvals
- Quality control in manufacturing
- Marketing campaign evaluations

And yes... catching shady latte dilution schemes.

## Summary: How Hypothesis Testing Works

| Step                        | Example |
|-----------------------------|---------|
| State H₀ and H₁             | H₀: Caffeine is 150mg; H₁: It's less |
| Collect data                | 7 caffeine samples |
| Choose significance level   | α = 0.05 |
| Compute test statistic      | Use t-test |
| Compare p-value to α        | If p < α, reject H₀ |

## Conclusion

Whether it’s coffee, company profits, or climate change — hypothesis testing gives us a way to **use evidence** instead of just gut feelings.

But yes — *sometimes your gut was right all along*. Especially about lattes.

Stay skeptical. Stay caffeinated.
