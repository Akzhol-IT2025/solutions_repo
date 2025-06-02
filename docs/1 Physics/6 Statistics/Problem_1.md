# Problem 1
Certainly! Here’s Statistics – Problem 1: Central Limit Theorem written in the same style and structure as your Mechanics Problem 1 on projectile motion:

⸻

Problem 1

Central Limit Theorem (CLT)

The Central Limit Theorem is a fundamental result in probability theory. It states that the sampling distribution of the sample mean of independent, identically distributed random variables approaches a normal distribution, regardless of the population’s original distribution, as the sample size increases.

This powerful idea explains why the normal distribution appears so often in statistics and real-world data.

⸻

To explore the Central Limit Theorem, we simulate sampling distributions from different population types and analyze their behavior.

⸻

1 – Population Distributions

We begin by selecting several population distributions:
	•	Uniform Distribution: All outcomes equally likely
	•	Exponential Distribution: Skewed, memoryless distribution
	•	Binomial Distribution: Discrete distribution from repeated Bernoulli trials

From each distribution, we generate a large population (e.g., 10,000 data points).

⸻

2 – Sampling and Mean Calculation

From each population, we take random samples of various sizes:

$$
n = 5,\ 10,\ 30,\ 50
$$

For each sample size:
	•	Take 1000 random samples
	•	Compute the sample mean of each
	•	Build a sampling distribution of the sample mean

As n increases, the shape of the sampling distribution tends toward a normal distribution.

⸻

3 – Behavior of Sampling Distribution

The sampling distribution of the mean has:
	•	A mean equal to the population mean:
$$
\mu_{\bar{x}} = \mu
$$
	•	A standard deviation (called the standard error):
$$
\sigma_{\bar{x}} = \frac{\sigma}{\sqrt{n}}
$$

This explains why larger samples produce less variable (narrower) distributions.

⸻

4 – Practical Interpretation

The CLT is crucial in applications such as:
	•	Estimating population parameters using sample means
	•	Quality control and setting control limits
	•	Polling and predicting public opinion
	•	Financial modeling and risk assessment

⸻

Summary

Term	Meaning
\mu	Population mean
\sigma	Population standard deviation
\bar{x}	Sample mean
\sigma_{\bar{x}}	Standard error = \sigma / \sqrt{n}
n	Sample size


⸻

Key Takeaway

Even if the original population is not normally distributed, the distribution of sample means becomes approximately normal as sample size increases — this is the essence of the Central Limit Theorem.