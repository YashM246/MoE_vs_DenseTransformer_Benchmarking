# MoE_vs_DenseTransformer_Benchmarking
# MoE vs. Dense Transformer Models: A Comprehensive Benchmark Study

## Project Overview

This repository contains the code, data, and analysis for our comparative benchmark study evaluating Mixture-of-Experts (MoE) architectures against traditional Dense Transformer models. The study provides a systematic evaluation of model capabilities across factual knowledge, reasoning, truthfulness, and bias dimensions.

## 🚀 Key Highlights

- Comprehensive evaluation of 6 state-of-the-art LLMs across 4 diverse datasets
- Rigorous comparison between sparse (MoE) and dense architectural paradigms
- 70+ hours of compute on A100 GPUs
- Novel insights into architectural trade-offs for real-world deployment

## 📊 Models Evaluated

| Model | Type | Parameters | Active Parameters |
|-------|------|------------|-------------------|
| Mixtral 8x7B 4-bit Quantized | MoE | 46.7B | 12.9B |
| RWKV-4-Raven-14B | Recurrent | 14B | 14B |
| DeepSeek v2 Base 7B | MoE | 15.7B | 2.4B |
| LLaMa 2 13B | Dense | 13B | 13B |
| Gemma 7B | Dense | 7B | 7B |
| Phi 3 mini 4k instruct | Dense | 3.8B | 3.8B |

## 📈 Datasets Used

1. **Counterfact Dataset** (200 samples)
   - Tests factual recall and knowledge integrity

2. **Bias Benchmark for Question Answering**
   - Age (200 Samples)
   - Disability (200 Samples)
   - Race (200 Samples)
   - Gender (200 Samples)

3. **TruthfulQA Dataset** (200 Samples)
   - Evaluates tendency to generate misinformation

4. **BigBench Logical Reasoning - 5 Object Logical Deduction** (200 Samples)
   - Tests pure reasoning capacity independent of knowledge

## 🔍 Key Findings

- Mixtral 8x7B outperformed all other models across all four datasets, demonstrating the effectiveness of the MoE architecture
- DeepSeek performed worst on bias metrics across all four demographic categories
- LLaMA 2 13B showed concerning weaknesses in the TruthfulQA benchmark
- RWKV-4-Raven model struggled most with factual recall and logical reasoning
- None of the models (except partially Mixtral) achieved above 60% accuracy on bias benchmarks

## 💡 Why This Matters

This benchmark provides critical insights into how architectural choices impact model performance across different dimensions. As LLMs become increasingly deployed in production environments, understanding these trade-offs becomes essential for responsible AI development.

