# 👋 Hi, I'm Viacheslav Kolupaev

Software Architect. I measure and model LLM inference: what it really costs to serve a model, where that cost comes from, and which levers move it.

I came to this from networks and data centers (CCNP/CCDP; designed and delivered a 50-rack, 200 kW facility). So when a serving system is slow or expensive, I check the queue, the scheduler and the placement before assuming it's the model.

### Latest measurement

**Closed-loop benchmarks run in synchronized waves.** With `--request-rate inf --max-concurrency 32` and identical requests, each request's TTFT includes the prefill of the whole wave: TTFT p50 1.33 s vs 0.09 s at concurrency 1 (vLLM, Qwen3-8B, 1× A100 80GB). A simple wave model predicts the mean TTFT within 1%.

→ [Experiment notes](https://github.com/vkolupaev/gpu-infra-lab/blob/main/experiments/2026-10-25-first-number.md) · [Docs PR to vLLM #63802](https://github.com/vllm-project/vllm/pull/63802)

### Focus

- **Inference serving:** vLLM, batching, KV cache, prefix-aware routing
- **Inference economics:** cost per 1M tokens, utilization, whole GPU vs MIG slice
- **GPU orchestration:** Kubernetes, MIG, multi-tenancy, topology-aware scheduling
- **Multi-GPU and fabric:** NCCL, InfiniBand / RoCE

Repos are working notebooks: method, raw numbers, and what didn't work.

🔗 [Site](https://vkolupaev.com) · [CV](https://vkolupaev.com/cv) · [LinkedIn](https://www.linkedin.com/in/vkolupaev/)
