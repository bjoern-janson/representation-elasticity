# Formalization

## 1. Representation Cost

Let a representation be:

\[
\phi: X \rightarrow Z
\]

where:

- \(X\) is observed reality
- \(Z\) is the internal representation
- \(\phi\) is the mapping that compresses observations into a usable structure

The representation cost is:

\[
L(\phi)
\]

where \(L\) measures the complexity required to construct and maintain the representation.

---

## 2. Predictive Sufficiency

A representation is valuable if it preserves the information required for prediction.

Define:

\[
P(Y|X) \approx P(Y|\phi(X))
\]

A successful representation removes irrelevant information while maintaining predictive ability.

The ideal representation minimizes:

\[
L(\phi)
\]

subject to:

\[
\text{Prediction Accuracy} \geq \epsilon
\]

---

## 3. Representation Elasticity

During learning, a system temporarily expands its representation:

\[
C(t)
\]

where \(C\) represents cognitive/model complexity over time.

Expansion phase:

\[
\Delta C_{expand} > 0
\]

Compression phase:

\[
\Delta C_{final} \ll \Delta C_{expand}
\]

Define elasticity:

\[
\mathcal{E}
=
\frac{\Delta C_{expanded}}
{\Delta C_{permanent}}
\]

High elasticity means the system can absorb complexity without retaining it.

---

## 4. Tool Metabolism

A tool introduces external computational structure:

\[
T \rightarrow O
\]

where:

- \(T\) = tool
- \(O\) = observations produced

A metabolizing system extracts:

\[
O \rightarrow M
\]

where \(M\) is an internal model.

Success condition:

\[
Performance(M)
\approx
Performance(T+M)
\]

The tool becomes optional after its structure is internalized.

---

## 5. Paradigm Failure

A representation fails when complexity grows faster than explanatory power.

Let:

\[
A_n
\]

represent accumulated adaptations/patches.

A paradigm shift trigger occurs when:

\[
\frac{dA_n}{dn} > \delta
\]

and a new representation exists:

\[
\exists \phi_2 :
\Omega(\phi_2) > \Omega(\phi_1)
\]

where \(\Omega\) represents explanatory efficiency.

---

## 6. The Core Optimization

The ultimate objective:

\[
\min_{\phi} L(\phi)
\]

subject to:

\[
P(Y|\phi(X)) \geq P_{target}
\]

The best intelligence is not the representation with maximum information.

It is the smallest representation that preserves the structure required to generate future predictions.
