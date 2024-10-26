# Awesome PEFT on MoE LLM

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A curated list of repositories in Parameter Finetuning Methods on Mixture of Experts Large Language Models.

## Papers

### PEFT for Instruction Tuning

#### 2024

- [MoDE: Effective Multi-task Parameter Efficient Fine-Tuning with a Mixture of Dyadic Experts](https://arxiv.org/pdf/2408.01505)
  - The paper introduces MoDE (Mixture of Dyadic Experts), a parameter-efficient fine-tuning method for multi-task adaptation of large language models. MoDE reduces redundancy by sharing a down-projection matrix across experts and introduces rank-one adapters for fine-grained task specialization. This approach allows for efficient and flexible multi-task learning, outperforming existing methods like LoRA and MoLORA on benchmarks while using comparable parameter budgets. MoDE’s design enhances parameter efficiency and expressiveness, making it well-suited for adapting language models to multiple tasks simultaneously.
- [AdaMoLE: Fine-Tuning Large Language Models with Adaptive Mixture of Low-Rank Adaptation Experts](https://arxiv.org/pdf/2405.00361)
  - The paper “AdaMoLE: Fine-Tuning Large Language Models with Adaptive Mixture of Low-Rank Adaptation Experts” presents an approach for parameter-efficient fine-tuning of LLMs using an Adaptive Mixture of Experts (MoE) framework. AdaMoLE dynamically adjusts the number of active LoRA experts based on the input context through an adaptive thresholding mechanism, enhancing task-specific performance without increasing the number of experts. It demonstrates significant improvements across various NLP tasks and commonsense reasoning benchmarks by optimizing the engagement of LoRA experts through a context-sensitive gating function.
- [HydraLoRA: An Asymmetric LoRA Architecture for Efficient Fine-Tuning](https://arxiv.org/pdf/2404.19245)
  - The paper “HydraLoRA: An Asymmetric LoRA Architecture for Efficient Fine-Tuning” proposes an architecture specifically designed to enhance parameter efficiency for LLMs. It introduces an asymmetric LoRA structure with a shared matrix A and multiple distinct B matrices to better capture various intrinsic components within a heterogeneous dataset. The approach integrates a Mixture-of-Experts (MoE) mechanism to dynamically handle B matrices during fine-tuning and inference, aiming to improve efficiency without relying on domain-specific knowledge.
- [MIXTURE OF LORA EXPERTS](https://arxiv.org/pdf/2404.13628)
  - The paper “Mixture of LoRA Experts (MOLE)” proposes a method for composing multiple Low-Rank Adaptation (LoRA) modules in a parameter-efficient manner. The main idea is to treat each layer of trained LoRAs as individual experts and use a gating function to dynamically determine the optimal composition weights. This approach addresses limitations in existing methods, such as the loss of individual characteristics during linear composition or high computational costs in reference tuning-based composition. MOLE aims to achieve a more efficient and flexible composition of LoRAs, enhancing performance in NLP and vision-language tasks while minimizing computational overhead.

#### 2023

- [SiRA: Sparse Mixture of Low Rank Adaptation](https://arxiv.org/pdf/2311.09179)
  - SiRA is a parameter-efficient tuning method that enhances LoRA by incorporating sparse Mixture of Experts (MoE) techniques. It activates a limited number of experts per input, uses expert dropout to prevent overfitting, and enforces capacity limits on the tokens each expert processes. These strategies improve computational efficiency and performance, allowing SiRA to outperform standard LoRA and other MoE-based approaches across various tasks with fewer parameters.
- [Pushing Mixture of Experts to the Limit: Extremely Parameter Efficient MoE for Instruction Tuning](https://arxiv.org/pdf/2309.05444)
  - The paper proposes a new way to fine-tune large language models more efficiently using a Mixture of Experts (MoE) approach. They introduce two methods, Mixture of Vectors (MoV) and Mixture of LoRA (MoLORA), which update less than 1% of the model’s parameters. These methods achieve nearly the same performance as fully fine-tuned models while being much more computationally efficient, especially for tasks the models haven’t seen before. A more detailed experiments is from [Scale AI](https://scale.com/blog/fine-tuning-mixture-of-experts-peft).
