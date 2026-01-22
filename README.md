## ML Inference Engineering

This repo is a collection of experiments around getting trained models to run fast in production. Most of the work focuses on what happens *after* training—exporting models, compiling them for specific hardware, squeezing out performance and actually serving them.

---

### Worklog

Running list of what's here. I'll add to this as I go.

- **Transformer Inference Acceleration: PyTorch to Torch-TensorRT**  *[[`Notebook`](transformer_torch_tensorrt.ipynb)]*
  Taking RoBERTa-base, compiling it with Torch-TensorRT in FP16 and FP32 modes, measuring the speedup and error analysis.  

- **Transformer Inference Acceleration: PyTorch to ONNX Export**  *[[`Notebook`](transformer_pytorch_onnx.ipynb)]*
  Taking a PyTorch Transformer model (RoBERTa-base), exporting it into ONNX format and measuring the speedup and error analysis. 

*(Will grow over time)*

---

### What's in here

Stuff I'm working on or have tried:

- Building inference pipelines from checkpoints
- Exporting models to ONNX, TorchScript, and other formats
- Using TensorRT, Torch-TensorRT, and similar tools to speed things up
- Quantization (FP32 → FP16 → INT8) and figuring out what breaks
- Benchmarking and profiling to see where time actually goes
- Setting up serving infrastructure (Triton, TorchServe)
- Understanding real tradeoffs between throughput, latency, and memory

---

### How it's organized

This isn't a polished library—it's more like a lab notebook:

- **Notebooks** for trying things out and showing results
- **Scripts** for benchmarks and repeatable experiments
- **Config files** for serving setups
- **Notes** on what worked, what didn't, and why

---

### Notes

- This is ongoing work—some things are half-finished
- Code here is for learning and experimentation, not necessarily production-ready

---

### Resources

- [NVIDIA TensorRT Quickstart Notebook Series](https://colab.research.google.com/github/NVIDIA/TensorRT/blob/main/quickstart/IntroNotebooks/0.%20Running%20This%20Guide.ipynb#scrollTo=pAKZqp7Qrjmq)