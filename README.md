# GraphRAG Quickstart

A step-by-step Jupyter notebook for getting Microsoft's [GraphRAG](https://github.com/microsoft/graphrag) running on your own computer: what it is, how to install it, indexing a sample book (*A Christmas Carol*), querying it with global, local, DRIFT and basic search, and exploring the resulting knowledge graph with pandas and networkx.

## Quick start

Requires **Python 3.11–3.13** and an **OpenAI API key**.

```bash
git clone <this repo>
cd graphrag-quickstart
python3.12 -m venv .venv
source .venv/bin/activate          # Windows: .venv\Scripts\activate
pip install -r requirements.txt
python -m ipykernel install --user --name graphrag --display-name "Python (graphrag)"
jupyter lab
```

Open `graphrag_quickstart.ipynb`, switch the kernel to **Python (graphrag)**, and run the cells top to bottom.

## Notes

- **Cost:** indexing makes many LLM calls. The notebook uses `gpt-4.1-mini` and `text-embedding-3-small` on a short book to keep costs low. Check your OpenAI usage afterwards.
- **Secrets:** your API key is entered with a hidden prompt and written to `christmas/.env`, which is git-ignored. Never commit it.
- **Generated files** (the `christmas/` project folder, index output, cache) are git-ignored.
