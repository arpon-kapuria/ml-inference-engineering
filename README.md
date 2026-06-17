<div align="center">

# ML Inference Engineering

**A collection of experiments on model optimization, inference acceleration, benchmarking and serving.**

<p>
<a href="https://www.python.org/"><img src="https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=FFD43B" alt="Python" /></a>
<a href="https://pytorch.org/"><img src="https://img.shields.io/badge/PyTorch-EE4C2C?logo=pytorch&logoColor=white" alt="PyTorch" /></a>
<a href="https://onnx.ai/"><img src="https://img.shields.io/badge/ONNX-005CED?logo=onnx&logoColor=white" alt="ONNX" /></a>
<a href="https://developer.nvidia.com/tensorrt"><img src="https://img.shields.io/badge/TensorRT-76B900?logo=nvidia&logoColor=white" alt="TensorRT" /></a>
<a href="https://vllm.ai/"><img src="https://img.shields.io/badge/vLLM-3776AF?logo=vllm&logoColor=FFD43B" alt="vLLM" /></a>
<a href="https://huggingface.co/"><img src="https://img.shields.io/badge/HuggingFace-FFD21E?logo=huggingface&logoColor=black" alt="Hugging Face" /></a>
</p>

</div>

<br>

## Worklog

| Category                  | Experiment                                                                            | Description                                                                                                     |
| ------------------------- | ------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| **Inference Acceleration** | **PyTorch → Torch-TensorRT** [[Notebook]](transformer_torch_tensorrt.ipynb)           | Compile RoBERTa-base with Torch-TensorRT (FP32/FP16), benchmark latency, and analyze output accuracy.           |
| **Inference Acceleration** | **PyTorch → ONNX** [[Notebook]](transformer_pytorch_onnx.ipynb)                       | Export RoBERTa-base to ONNX and evaluate inference performance and numerical differences.                       |
| **Inference Acceleration** | **PyTorch → ONNX → TensorRT** [[Notebook]](transformer_pytorch_onnx_tensorrt.ipynb)   | Convert a PyTorch model to ONNX and TensorRT, then benchmark speed and output fidelity.                         |
| **Model Optimization**    | **LLM Compressor (GPTQ W4A16)** [[Notebook]](model_optimization_llm_compressor.ipynb) | Apply post-training quantization and compare compressed and full-precision models.                              |
| **LLM Serving**           | **vLLM Inference Server** [[Notebook]](serving_llms_with_vllm.ipynb)                  | Deploy a vLLM server and explore continuous batching, KV cache management, prefix caching, and serving metrics. |
| **Benchmarking & Evaluation** | **GuideLLM and LM Evaluation** [[Notebook]](benchmarking_evaluation_vllm.ipynb) | Benchmark vLLM deployment's latency and throughput using GuideLLM, evaluate model quality with LM Evaluation Harness, and analyze performance–quality trade-offs for deployment decisions. |

<sub><i>( Will grow over time )</i></sub>

## Topics

- Post-Training Workflows
- Model Optimization & Quantization
- Inference Acceleration
- LLM Serving & Deployment
- Benchmarking & Profiling
- Throughput, Latency & Memory Trade-offs


## Notes

- This is ongoing work—some things are half-finished
- Code here is for learning and experimentation, not necessarily production-ready

## License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).
