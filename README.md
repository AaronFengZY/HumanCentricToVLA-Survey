<div align="center">


  <h1>From Human Videos to Robot Manipulation: A Survey on Action-Relevant Representation Transfer for Scalable Vision-Language-Action Learning</h1>

  <p>
    <img src="https://img.shields.io/badge/Status-Under_Review-important?style=for-the-badge" alt="Status: Under Review">
  </p>

</div>

## 📝 Abstract

Recent progress in generalizable embodied control has been driven by large-scale pretraining of Vision–Language–Action (VLA) models. However, most existing approaches rely on large collections of robot demonstrations, which are costly to obtain and tightly coupled to specific embodiments.

Human videos, by contrast, are abundant and capture rich interactions. Yet, embodiment differences and the frequent absence of task-aligned annotations make their direct use in VLA models challenging.

**This survey provides a unified view of how human videos are transformed into effective knowledge for VLA models.** We categorize existing approaches into four classes based on the action-related information they derive, and highlight key open challenges in structuring videos, grounding supervision, and evaluation.

---

## 🧭 Taxonomy: Action-Relevant Representations

To bridge the gap between passive human observation and active robot control, we identify four distinct routes based on the **nature of the constructed representations** (see **Figure 1** in the paper):

* **Latent Action Abstraction**
    * *Definition:* Circumvents explicit alignment by encoding inter-frame changes or intents into discrete codes or continuous embeddings.
* **Predictive World Modeling**
    * *Definition:* Uses video as a source of predictive learning signal to forecast future outcomes and distill these representations into policies.
* **Explicit 2D Cues**
    * *Definition:* Extracts interpretable image-plane signals—such as point tracks, masks, or flow—using off-the-shelf vision tools.
* **Explicit 3D Structure**
    * *Definition:* Recovers 3D structure (poses/trajectories) to retarget motion into robot-compatible action spaces.

---

## 💡 Contributions

1.  **Signal-centric Taxonomy:** We introduce a pipeline-based taxonomy of *representation bridges* that transform human videos into action-relevant representations, comparing the four routes in terms of representation form, scalability, and grounding requirements.
2.  **Dataset Map & Available Signals:** We systematize representative human-video datasets along two axes—the availability of explicit geometric/3D signals and scripted vs. in-the-wild collection—and summarize how different supervision affordances support different transfer pipelines.
3.  **Challenges at Three Interfaces:** We distill open problems at three critical interfaces:
    * Scalable episodization of unstructured videos.
    * Heterogeneity-aware grounding under embodiment/viewpoint mismatch.
    * Deployment-predictive evaluation for transfer efficiency.

### Taxonomy Figure
<p align="center">
  <img src="figures/tree.jpg" alt="Taxonomy tree of human-video-to-robot transfer" width="900">
</p>
<p align="center">
  <em>Figure: Taxonomy landscape of human-video-to-robot transfer methodologies.</em>
</p>


## 📌 Paper List by Paradigm

### (I) Latent Actions Papers

| Paper | Date |
| --- | --- |
| [LAPA](https://arxiv.org/abs/2410.11758) | 2024-10 |
| [IGOR](https://arxiv.org/abs/2411.00785) | 2024-10 |
| [Moto](https://arxiv.org/abs/2412.04445) | 2024-12 |
| [GO-1](https://arxiv.org/abs/2503.06669) | 2025-03 |
| [GR00T](https://arxiv.org/abs/2503.14734) | 2025-03 |
| [UniVLA](https://arxiv.org/abs/2505.06111) | 2025-05 |
| [Villa-X](https://arxiv.org/abs/2507.23682) | 2025-07 |
| [ViPRA](https://arxiv.org/abs/2511.07732) | 2025-11 |
| [LAWM](https://arxiv.org/abs/2512.10016) | 2025-12 |
| [Motus](https://arxiv.org/abs/2512.13030) | 2025-12 |
| [CLAP](https://arxiv.org/abs/2601.04061) | 2026-01 |


### (II) World Models

| Paper | Date |
| --- | --- |
| [GR-1](https://arxiv.org/abs/2312.13139) | 2023-12 |
| [Gen2Act](https://arxiv.org/abs/2409.16283) | 2024-09 |
| [GR-2](https://arxiv.org/abs/2410.06158) | 2024-10 |
| [VPP](https://arxiv.org/abs/2412.14803) | 2024-12 |
| [FLARE](https://arxiv.org/abs/2505.15659) | 2025-05 |
| [mimic-video](https://arxiv.org/abs/2512.15692) | 2025-12 |

### (III) Explicit 2D

| Paper | Date |
| --- | --- |
| [ATM](https://arxiv.org/abs/2401.00025) | 2023-12 |
| [Magma](https://arxiv.org/abs/2502.13130) | 2025-02 |
| [Gemini Robotics](https://arxiv.org/abs/2503.20020) | 2025-03 |
| [A0](https://arxiv.org/abs/2504.12636) | 2025-04 |
| [Masquerade](https://arxiv.org/abs/2508.09976) | 2025-08 |

### (IV) Explicit 3D Papers

| Paper | Date |
| --- | --- |
| [VidBot](https://arxiv.org/abs/2503.07135) | 2025-03 |
| [EgoVLA](https://arxiv.org/abs/2507.12440) | 2025-07 |
| [Being-H0](https://arxiv.org/abs/2507.15597) | 2025-07 |
| [H-RDT](https://arxiv.org/abs/2507.23523) | 2025-07 |
| [MotionTrans](https://arxiv.org/abs/2509.17759) | 2025-09 |
| [Yoshida et al.](https://arxiv.org/abs/2509.21986) | 2025-09 |
| [VITRA](https://arxiv.org/abs/2510.21571) | 2025-10 |
| [In-N-On](https://arxiv.org/abs/2511.15704) | 2025-11 |
| [Simar et al.](https://arxiv.org/abs/2512.22414) | 2025-12 |
---

## 🧩 Open challenges highlighted in the paper

We organize future directions around three interfaces:
1. **Episodization:** turning web-scale, untrimmed videos into training-ready episodes  
2. **Heterogeneity-aware grounding:** embodiment mismatch (human hand vs robot EE) + viewpoint mismatch (exo/ego vs robot cameras)  
3. **Benchmarking:** evaluation protocols that predict **real deployment performance** and **transfer efficiency under a robot-data budget**
