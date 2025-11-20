# CIx
The Contextual Integrity Index (CIx): A Dual-Axis, Physics-Inspired Framework for LLM Hallucination Measurement

The Contextual Integrity Index (\boldsymbol{CIx})
The \boldsymbol{CIx} is a novel, dual-axis, physics-inspired framework designed for the precise, diagnostic measurement of Large Language Model (LLM) hallucination and reliability. It moves beyond traditional single-aggregate metrics by quantifying both the rate and the structural consistency of factual errors in LLM output.
1. The Core Problem and Solution
Existing LLM reliability scores often rely on simple proportional aggregates, which fail to capture the local positional volatility of factual claims within a generated text. A document with a few highly concentrated errors and a document with errors scattered erratically might receive the same overall score, despite representing vastly different failure modes.
The \boldsymbol{CIx} addresses this by defining LLM integrity as a vector in a two-dimensional diagnostic space, enabling precise classification of failure types.
2. Framework Inputs
The entire framework is contingent on a robust, pre-computed or internally-derived token-level Grounding Confidence Signal (C_t), where C_t \in [0, 1]. This signal represents the confidence that the content of each token is grounded in verifiable fact.
3. Dual-Axis Components
The \boldsymbol{CIx} is defined as a vector: \boldsymbol{CIx} = (\boldsymbol{HM}_{\text{ERR}}, \boldsymbol{HM}_{\text{FFT}}), composed of two orthogonal metrics:
X-Axis: Systemic Error Rate (\boldsymbol{HM}_{\text{ERR}})
This component measures the overall proportion of unsupported content, drawing an analogy from AC Power Quality Analysis.
• Analogy: Defines Grounded Truth (High C_t) as Active Power (P) and Hallucination (Low C_t) as Reactive Power (Q).
• Measurement: Quantifies the ratio of ungrounded content (Q) to the total generative capacity (S = P+Q).
• Purpose: Provides the necessary aggregate error rate—a foundational measure of how much generative capacity is dedicated to unsupported claims.
