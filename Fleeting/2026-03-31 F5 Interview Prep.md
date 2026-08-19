Oftentimes for security, a false positive (blocking a legitimate user) is considered just as bad as a false negative (letting an attacker through).

Approach: Treat security as a **risk score**
- Low risk: Pass through
- Medium risk: Challenge (CAPTCHA, MFA, rate-limit/throttle)
- High risk: Block

## Terms

**Model drift**: A model gets progressively worse as the nature of the input changes (e.g. an iOS update).
- Key idea: Use **shadow mode**: Run a new version of the model in parallel, but don't let the new one block traffic until accuracy is verified

**Schema validation**: Ensuring data conforms to a predefined structure.
**Deterministic vs. Probabilistic**: Hard-coded rules vs. statistical guesses.
**Zero trust**: Every request is treated as hostile.
**Canary deployment**: Rolling out a feature to 1% of users to check for bugs.
**Feature attribution**: Understanding which input causes the AI to flag a request. Need for explaining to a customer why they were blocked.
**Adversarial attack**: Deliberately manipulating input to deceive machine learning models.
**Data poisoning**: Maliciously corrupting training data to create a backdoor.
- Key idea: Use **data cleaning** and only use data from trusted sources.

**Input sanitisation**: Cleaning/normalising data before it hits the model.
**Denoising**: Removing "noise" from inputs to restore the original signal.
**Inference latency**: The time it takes for a model to generate a prediction.
**Throughput**: Requests per second.
**Observability**: Tracking metrics, logs, and traces to see what's happening.
**Circuit breaker pattern**: Automatically disabling a feature if it starts failing.