---
title: "RedVTP: Training-Free Acceleration of Diffusion Vision-Language Models Inference via Masked Token-Guided Visual Token Pruning"
permalink: /publication/redvtp/
year: 2026
order: 1
status: "Accepted"
selected: true
authors: "Jingqi Xu*, Jingxi Lu*, Chenghao Li*, Sreetama Sarkar, Souvik Kundu, Peter A. Beerel"
venue: "CVPR 2026 Findings"
excerpt: "A response-driven visual-token pruning method that accelerates diffusion vision-language model inference while preserving benchmark accuracy."
paperurl: "https://arxiv.org/abs/2511.12428"
codeurl: "https://github.com/Blacktower27/RedVTP"
---

RedVTP estimates visual-token importance from the attention of still-masked
response tokens. It prunes less important visual tokens after the first
diffusion inference step, reducing latency by up to 64.97% and increasing
token-generation throughput by up to 186% on the evaluated models.

\* Equal contribution.
