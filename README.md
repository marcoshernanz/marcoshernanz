## Marcos Hernanz

Software engineer working on language-model training.

Most recently a Software Engineer Intern on the Next.js team at Vercel, where I built an AI maintainer for Next.js and used it to [close 1,500 GitHub issues in one month](https://nextjs.org/blog/how-we-closed-1500-github-issues).

### Research

- **Bachelor's thesis** at UAM, advised by Daniel Hernández-Lobato: how Muon versus AdamW shapes routing in DeepSeek-style mixture-of-experts language models. I built the PyTorch training stack (grouped-matmul experts, batched Muon, `torch.compile`, bitwise-exact resume) and ran **145 pre-registered runs** at 55M and 108M active parameters. Muon makes the load balancer work harder, and the backbone's optimizer, not the router's, causes it through a shared direction in the router's inputs.
<!-- TODO: add the arXiv link once the paper is announced. -->
- **[Multi-Head mHC: No Gain at Equal Parameters](https://hernanz.io/multi-head-mhc.pdf)** (preprint, October 2026; [code](https://github.com/marcoshernanz/multi-head-mhc)). A multi-head variant of manifold-constrained hyper-connections (mHC), tested in **629 TPU training runs** of 27M- and 112M-parameter GPT models on FineWeb-Edu against parameter-matched controls: **no gain at equal parameters**.

### Vercel, Next.js team

- Built an **AI maintainer for Next.js** that investigates GitHub and customer reports end to end, from triage and reproduction through canary verification, regression bisection, tests, and fixes.
- Ran it as a human-reviewed queue that [**closed 1,500 GitHub issues in one month**](https://nextjs.org/blog/how-we-closed-1500-github-issues), taking the open backlog from **2,244 to 995** with **3 reopens**, and wrote the Next.js blog post on the campaign.
- Owned the product and agent stack behind it, including resumable specialist workflows, model routing, cost and evaluation tracing, and an **Eve** harness benchmark on **Terminal-Bench 2.1**.
- Shipped **Next.js Agent Feedback**, a human-in-the-loop path where coding agents draft deidentified reports on the framework friction they hit and the developer edits, sends, or discards each one before anything is submitted.
- Merged **22 Next.js and Turbopack PRs** plus upstream **SWC** and **notify-rs** fixes, including a [**42×** HMR invalidation speedup](https://github.com/vercel/next.js/pull/96137), a [React Compiler precheck](https://github.com/vercel/next.js/pull/96820) that cut compiler pipeline time **19.64%** on real v0 modules, and a [worker-lifecycle fix](https://github.com/vercel/next.js/pull/96592) that eliminated **100%** of measured worker leak growth.
- Found a **cross-tenant data leak** in Vercel Sandbox's Linux device-mapper storage layer, credited by name in [Vercel's write-up of the $1M Sandbox challenge](https://vercel.com/blog/findings-from-the-1-million-dollar-vercel-sandbox-challenge).

### Projects

- **[llm-internals](https://github.com/marcoshernanz/llm-internals):** how a modern LLM works, built from scratch.
  - **Architecture:** reimplemented DeepSeek-V4.1-Flash from its technical report: compressed sparse attention with a top-k indexer, mHC with Sinkhorn mixing, Engram n-gram memory and the DSpark draft head.
  - **Kernels:** hand-wrote fused **Triton** RMSNorm forward and backward kernels and their autograd function, with the weight gradient accumulated in per-SM partial sums.
  - **Post-training:** reimplemented **Qwen3-0.6B** in plain PyTorch with a batched KV-cache sampler, then wrote full-parameter **SFT** with assistant-only loss and sequence packing that took zero-shot GSM8K from **6% to 52%**.
  - Fused the head into a chunked cross-entropy, so 4,096-token steps fit in 18.7 GiB where the plain loss runs out of memory.
- **[llm-lab](https://github.com/marcoshernanz/llm-lab):** a language-model training lab, from bigrams to Transformers.
  - Wrote a byte-level BPE tokenizer and a 10B-token FineWeb-Edu pipeline.
  - Trained a 13.7M-parameter Transformer in JAX on **8 TPU v5e chips**: **39.85B tokens at 2.63M tokens/s**.
  - Grew a small PyTorch decoder one modern mechanism per run across 18 runs: RoPE, GQA, MLA, hybrid attention, a 64-expert MoE with loss-free balancing, Kimi Delta Attention, attention residuals and multi-token prediction.
- **[BareTensor](https://github.com/marcoshernanz/baretensor):** a PyTorch-style tensor and autograd library, written from scratch in **C++**.
  - Strided tensors, broadcasting, dynamic autograd, neural-network modules and Python bindings.
  - Trained language models with it, from bigrams up to self-attention.
- **[ChatVault](https://github.com/marcoshernanz/ChatVault):** private semantic search for WhatsApp.
  - Runs locally in the browser with quantized MiniLM, **Rust** and **WebAssembly**.
  - Finding and reproducing a Turbopack issue while building it led directly to my off-cycle Vercel internship.
- **[Cogniba](https://github.com/cogniba/cogniba):** a brain-training product.
  - Designed, built and launched it with **Next.js** and **Supabase**.
  - Grew it to more than **2,000 registered users**.

### Competitive programming

- **Codeforces Expert** with a peak rating of 1800
- 2x **ICPC SWERC** participant
- **Olympiad in Informatics**, 2nd in Madrid and 16th in Spain
- 3x Meta Hacker Cup Top 2,000
- 2x Ada Byron Spanish national finalist

### Contact

[X](https://x.com/MarcosHernanz) | [LinkedIn](https://www.linkedin.com/in/marcoshernanz/) | [Email](mailto:marcos@hernanz.io)
