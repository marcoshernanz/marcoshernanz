## Marcos Hernanz

I build coding agents, evaluation infrastructure, ML systems, and performance-sensitive developer tools.

Most recently a Software Engineer Intern on the Next.js team at Vercel, where I built an AI maintainer for Next.js and used it to [close 1,500 GitHub issues in one month](https://nextjs.org/blog/how-we-closed-1500-github-issues).

### Vercel, Next.js team

- Built an **AI maintainer for Next.js** that investigates GitHub and customer reports end to end, from triage and reproduction through canary verification, regression bisection, tests, and fixes.
- Ran it as a human-reviewed queue that [**closed 1,500 GitHub issues in one month**](https://nextjs.org/blog/how-we-closed-1500-github-issues), taking the open backlog from **2,244 to 995** with **3 reopens**, and wrote the Next.js blog post on the campaign.
- Owned the product and agent stack behind it, including resumable specialist workflows, model routing, cost and evaluation tracing, and an **Eve** harness benchmark on **Terminal-Bench 2.1**.
- Shipped **Next.js Agent Feedback**, a human-in-the-loop path where coding agents draft deidentified reports on the framework friction they hit and the developer edits, sends, or discards each one before anything is submitted.
- Merged **26 Next.js and Turbopack PRs** plus upstream **SWC** and **notify-rs** fixes, including a [**42×** HMR invalidation speedup](https://github.com/vercel/next.js/pull/96137), a [React Compiler precheck](https://github.com/vercel/next.js/pull/96820) that cut compiler pipeline time **19.64%** on real v0 modules, and a [worker-lifecycle fix](https://github.com/vercel/next.js/pull/96592) that eliminated **100%** of measured worker leak growth.

### Projects

- **[llm-lab](https://github.com/marcoshernanz/llm-lab):** Language-model training and systems laboratory, built from bigrams through Transformers with tokenization, FineWeb-Edu data pipelines, profiling, checkpointing, and multi-device training. Trained a Transformer across **8 TPU v5e devices**, processing **39.85B training tokens at 2.63M tokens/s**. Rebuilt that baseline into a **2026-era architecture** through a cumulative ladder of 18 controlled experiments covering RoPE, GQA, SwiGLU, RMSNorm, MLA, mixture-of-experts, Kimi Delta Attention, and multi-token prediction. Hand-wrote a **Muon** optimizer that matched `torch.optim.Muon` from identical initialization.
- **[BareTensor](https://github.com/marcoshernanz/baretensor):** Built a near-zero-dependency tensor and autograd runtime from scratch in **C++**, with strided tensors, broadcasting, neural-network operations, dynamic autograd, and Python bindings.
- **[ChatVault](https://github.com/marcoshernanz/ChatVault):** Built private semantic search for WhatsApp that runs locally in the browser using quantized MiniLM, **Rust**, and **WebAssembly**. Finding and reproducing a Turbopack issue while building it led directly to my off-cycle Vercel internship.
- **[Cogniba](https://github.com/cogniba/cogniba):** Designed, built, and launched a brain-training product with **Next.js** and **Supabase**, growing it to more than **2,000 registered users**.

### Competitive programming

- **Codeforces Expert** with a peak rating of 1800
- 2x **ICPC SWERC** participant
- **Olympiad in Informatics**, 2nd in Madrid and 16th in Spain
- 3x Meta Hacker Cup Top 2,000
- 2x Ada Byron Spanish national finalist

### Contact

[X](https://x.com/MarcosHernanz) | [LinkedIn](https://www.linkedin.com/in/marcoshernanz/) | [Email](mailto:marcos.hernanz.anton@gmail.com)
