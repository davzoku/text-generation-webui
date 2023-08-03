# Set-up Guide

## Apple Silicon M1

[Updated Oobabooga Textgen WebUI for M1/M2 [Installation & Tutorial] - YouTube](https://www.youtube.com/watch?v=btmVhRuoLkc)

[Fix for MPS support on Apple Silicon by WojtekKowaluk · Pull Request #393 · oobabooga/text-generation-webui](https://github.com/oobabooga/text-generation-webui/pull/393)

1. Run the following commands specifically to set up

```
conda create -n textgen python=3.10.10
conda active textgen
python -m pip install -r requirements.txt
pip install -U --pre torch torchvision -f https://download.pytorch.org/whl/nightly/cpu/torch_nightly.html
```

2. Run the following commands to start with best performance

```
python server.py --threads 6
```

Choose the threads based on your machine

```
M1/M2: --threads 4
M1/M2 Pro (8 cores) --threads 6
M1/M2 Pro (10 cores) --threads 8
M1/M2 Max: --threads 8
M1 Ultra: --threads 16
```

3. Use the UI to install LLMs from huggingface or place the downloaded .bin files in the `models/` folder.

4. Load the model and start playing!
