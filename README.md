# Documentação CAETE

**Este repositório possui um **[Github Actions](.github/workflows/deploy-sphinx.yml)** configurado para fazer deploy automático da documentação utilizando sphinx.

## Build

```bash
python -m venv ~/sphinx
source activate ~/sphinx
pip install -r docs/requirements.txt
sphinx-build -b html docs/ _build/html
```