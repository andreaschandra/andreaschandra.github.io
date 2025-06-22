---
title: "Large Language Models for Code Generation"
read_time: false
categories:
  - research
tags:
  - llm
image:
  feature: codegeneration.png
  thumb: codegeneration.png
---

![alt]({{ site.url }}{{ site.baseurl }}/assets/images/codegeneration.png)


Large Language Models (LLMs) have gained a remarkable achievement across diverse general tasks and programming tasks. LLMs role in code generation covers from the simplest form such as code completion to code generation from natural language. This post provides a brief introduction and resources needed to train or fine-tune LLMs to be able to generate code from base model.

## Tasks

There are 7 code generation tasks that LLMs are capable of:
1. Code completion, recommends the next chunk of code from a given starter code or associated description such as docstring to speed up the development and preciseness.
2. Code translation, translate the code from one programming language to another while maintaining the same purpose and process.
3. Code repair, identify existing a chunk of code by generating the correct version, usually for clarity, simplicity, and optimized.
4. Code summarization, generate textual description or explaination from a chunk of code or the entire code base to give understanding the process as well as docstring to give specific documentation.
5. Code generation, which known as vibe coding, generate a snippet of code or the entire code base by using prompt to automate development. 



## Code Generation Dataset
Despite the abundance of training resources, it may refers to the same sources or added another sources that may contain duplication. Hence, large corpus gives two version, one full set and another is deduplication. One who want to train is usually using deduplication. During this analysis, I found the main sources of creating this dataset is mainly from Github as the primary platform to share open source software. The dataset that claims large dataset maybe is not that large as it claims nor diverse as it seemed.

- CodeSearchNet is a collection of datasets and benchmarks that explore the problem of code retrieval using natural language. The dataset contains 2 million commend, code pairs in Python, Javascript, Ruby, Go, Java and PHP code. The dataset source is from Github with the size of 20GB. [Github](https://github.com/github/CodeSearchNet) [HF Dataset](https://huggingface.co/datasets/irds/codesearchnet)

- Google BigQuery a full snapshot of the content of more than 2.8 million open source GitHub repositories in BigQuery. [Post](https://cloud.google.com/blog/topics/public-datasets/github-on-bigquery-analyze-all-the-open-source-code)

- The Pile is a 825 GiB diverse, open source language modelling data set that consists of 22 smaller, high-quality datasets combined together. The dataset is built on top of smaller datasets such as PubMed Central, ArXiv, Github, the FreeLaw Project, Stack Exchange, the US Patent and Trademark Office, PubMed, Ubuntu IRC, HackerNews, YouTube, PhilPapers, and NIH ExPorter, Books3, Project Gutenberg, Open-Subtitles, English Wikipedia, DM Mathematics, EuroParl, and the Enron Emails corpus. [Page](https://pile.eleuther.ai/) [HF Dataset](https://huggingface.co/datasets/EleutherAI/pile)

- Code Parrot contains approxiamtely 22 million Python files from Google's Bigquery with 180 GB in size. [HF Dataset](https://huggingface.co/datasets/transformersbook/codeparrot)

- Github Code consists of 115M code files from GitHub in 32 programming languages with 60 extensions totaling in 1TB of data. The dataset was created from the public GitHub dataset on Google BiqQuery. [HF Dataset](https://huggingface.co/datasets/codeparrot/github-code)

- ROOTS contains a 1.6TB dataset with 59 natural languages nad 13 programming languages that was used to train BLOOM model. The dataset contains free text and code bases. [Paper](https://arxiv.org/pdf/2303.03915) [HF Dataset](https://huggingface.co/bigscience-data/datasets)

- The Stack is a 6.4 TB comprehensive collection of open-source code files from 358 programming languages, developed by the BigCode Project to train AI models that generate code. These Code LLMs can create programs based on natural language instructions or modify existing code snippets. [HF Dataset](https://huggingface.co/datasets/bigcode/the-stack)

- The Stack v2 is a 67.5 TB with 600+ programming and markup languages. The dataset is collected from the Software Heritage archive. [HF Dataset](https://huggingface.co/datasets/bigcode/the-stack-v2)

## Reference
[1] Juyong Jiang et al. [A Survey on Large Language Models for Code Generation](A Survey on Large Language Models for Code Generation). 2024