# LAG - Limitless Autonomous Guardian

LAG1 is an open-source large language model built with TensorFlow, featuring cross-thinking architecture for enhanced reasoning capabilities. This project aims to create a chatty, coding-aware assistant that matches GPT-4 quality while remaining open and hackable.

## 🌟 Features

- **🧠 Cross-Thinking Architecture**: Dual-stream reasoning with primary and reflection paths
- **🔄 Multi-Path Generation**: Explore multiple reasoning approaches simultaneously  
- **🛠️ Flexible Tokenization**: Works with Hugging Face tokenizers or TensorFlow Text
- **📊 Comprehensive Datasets**: Supports 6 diverse datasets including math, coding, and reasoning
- **🚀 Production Ready**: Includes FastAPI server generation and deployment utilities
- **🔧 Advanced Reasoning**: Chain-of-thought, self-correction, consensus mechanisms

## 🚀 Quick Start

1. **Clone the repository**:
   ```bash
   git clone https://github.com/NaveenSingh9999/LAG.git
   cd LAG
   ```

2. **Open the Jupyter notebook**:
   ```bash
   jupyter notebook lag1.ipynb
   ```

3. **Run the smoke test** to verify everything works:
   ```python
   smoke_test_lag1()
   ```

4. **Authenticate for gated datasets** (optional):
   ```bash
   huggingface-cli login
   ```

5. **Train your first model**:
   ```python
   full_training_pipeline_demo()
   ```

## 📚 Datasets

LAG1 trains on a diverse mix of high-quality datasets:

- **fka/awesome-chatgpt-prompts**: Creative conversation starters
- **openai/gdpval**: Policy-compliant responses (requires auth)
- **GeoGPT-Research-Project/GeoGPT-QA**: Geospatial knowledge (requires auth)
- **openai/gsm8k**: Grade-school math reasoning
- **nebius/SWE-rebench**: Software engineering tasks (requires auth)
- **HuggingFaceH4/MATH-500**: Graduate-level mathematics

## 🧠 Advanced Reasoning

LAG1 includes several advanced reasoning capabilities:

### Multi-Step Reasoning
```python
reasoning_result = multi_step_reasoning(
    model, tokenizer_mgr, 
    "Solve the equation 2x + 5 = 13", 
    config
)
```

### Self-Correction
```python
corrected = self_correction_loop(
    model, tokenizer_mgr, 
    initial_answer, question, config
)
```

### Consensus Reasoning
```python
consensus = consensus_reasoning(
    model, tokenizer_mgr, 
    "Explain photosynthesis", 
    config, num_agents=5
)
```

## 🚀 Production Deployment

Generate a production-ready FastAPI server:

```python
export_for_deployment(
    trainer, tokenizer_mgr, 
    "/path/to/export", 
    include_server=True
)
```

Then run the server:
```bash
cd /path/to/export
pip install -r requirements.txt
python server.py
```

## 🔧 Configuration

Customize LAG1 through the `Lag1Config` class:

```python
config = Lag1Config(
    vocab_size=32000,
    max_position_embeddings=1024,
    hidden_size=768,
    num_layers=12,
    num_heads=12,
    cross_thinking_heads=6,
    intermediate_size=3072,
    dropout_rate=0.1
)
```

## 📊 Architecture

LAG1 features a novel cross-thinking architecture:

1. **Dual-Stream Processing**: Each decoder block maintains separate primary and reflection streams
2. **Cross-Attention**: Streams share information through gated cross-attention mechanisms
3. **Thought Cache**: Optional buffer for storing intermediate reasoning states
4. **Reflection Integration**: Reflection stream influences final generation through learned gates

## 🤝 Contributing

We welcome contributions! Please see our contributing guidelines for details.

## 📄 License

This project is open source. Please see the LICENSE file for details.

## 🙏 Acknowledgments

- Built with TensorFlow and Hugging Face Transformers
- Inspired by chain-of-thought reasoning research
- Dataset providers: OpenAI, Hugging Face, and the open source community

## 📞 Contact

For questions and support, please open an issue on GitHub.

---

**LAG - Making AI reasoning transparent and accessible to everyone.**