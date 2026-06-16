## ML Inference Engineering

This repo is a collection of experiments around getting trained models to run fast in production. Most of the work focuses on what happens *after* training—exporting models, compiling them for specific hardware, squeezing out performance and actually serving them.

---

### Worklog

Running list of what's here. I'll add to this as I go.

- **Transformer Inference Acceleration: PyTorch to Torch-TensorRT**  *[[`Notebook`](transformer_torch_tensorrt.ipynb)]*<br>
  Taking RoBERTa-base, compiling it with Torch-TensorRT in FP16 and FP32 modes, measuring the speedup and error analysis.  

- **Transformer Inference Acceleration: PyTorch to ONNX Export**  *[[`Notebook`](transformer_pytorch_onnx.ipynb)]*<br>
  Taking a PyTorch Transformer model (RoBERTa-base), exporting it into ONNX format and measuring the speedup and error analysis. 
- **Transformer Inference Acceleration: PyTorch to ONNX to TensorRT** *[[`Notebook`](transformer_pytorch_onnx_tensorrt.ipynb)]*<br>
  Taking a PyTorch Transformer model (RoBERTa-base), exporting it into ONNX format, then to TensorRT and measuring the speedup and error analysis.
- **Model Optimization using LLM Compressor** *[[`Notebook`](model_optimization_llm_compressor.ipynb)]*<br>
  See how **post-training quantization** works via full precision & compressed model comparisons. Use the `llm-compressor` library to apply a GPTQ recipe that produces a W4A16 quantized model. Test and evaluate the quantized model against the original

<sub><i>(Will grow over time)</i></sub>

---

### What's in here

Stuff I'm working on or have tried:

- Building inference pipelines from checkpoints
- Exporting models to ONNX, TorchScript, and other formats
- Efficient model optimization and serving
- Quantization and figuring out what breaks
- Benchmarking and profiling to see where time actually goes
- Setting up serving infrastructure
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

### License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).