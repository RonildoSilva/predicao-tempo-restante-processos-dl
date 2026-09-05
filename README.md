# Predição de tempo restante de processos de negócio com aprendizado profundo

> Código, notebooks e resultados do artigo *Predição de tempo restante para conclusão de processos de negócio utilizando aprendizado profundo*: seis arquiteturas neurais comparadas em cinco logs de eventos, com intervalos de confiança e reprodução de trabalhos da literatura.

![status](https://img.shields.io/badge/status-concluído-success) ![python](https://img.shields.io/badge/Python-3-blue) ![tf](https://img.shields.io/badge/TensorFlow-Keras-orange) ![jupyter](https://img.shields.io/badge/Jupyter-notebooks-orange)

## Sobre
Pesquisa de mestrado (2023) em mineração de processos preditiva. A predição do tempo restante de uma instância de processo ajuda a evitar esperas incertas, revelar gargalos e apoiar sistemas de atendimento. Foram avaliadas, sobre prefixos de traços, as arquiteturas **SA-BiLSTM**, **SA-Dense**, **Dense**, **BiLSTM-SA**, **BiLSTM** e **Transformer Encoder**, além de regressores clássicos como baseline, medindo MAE com intervalos de confiança.

Logs de eventos: três processos de uma secretaria de fazenda estadual (`A_25`, `A_50`, `A_75`, por assunto e percentil de tamanho de prefixo), **BPI Challenge 2012** e **Helpdesk 2017**. Os dados tratados estão no repositório [datasets](https://github.com/RonildoSilva/datasets).

## Estrutura de pastas
```text
Experimentos do Autor/Arquiteturas Propostas/
├── A_25/, A_50/, A_75/, BPI 12/, Helpdesk 17/
│   ├── Notebooks/         A) SA_BiLSTM … F) TRANSFORMER_ENCODER
│   └── Resultados/        Algoritmos - Baseline, Arquiteturas
└── Cálculos Intervalos de confiança/   CI SFZ.py e planilhas de MAE
Reprodução de Experimentos - Literatura/
├── Experimentos/Bukhsh Silva/   ProcessTransformer (Bukhsh et al.) nos mesmos logs
├── Experimentos/Navarin Silva/  DA-LSTM (Navarin et al.) em BPI12 e HD17
└── Cálculos Intervalos de confiança/
```
Reproduções adicionais estão em [reproducao-experimentos-ppm](https://github.com/RonildoSilva/reproducao-experimentos-ppm).

## Como executar
Os notebooks foram executados no Google Colab; cada um baixa seus CSVs do repositório `datasets` e fixa `seed(42)`.
```bash
pip install tensorflow pandas numpy scikit-learn matplotlib
jupyter notebook "Experimentos do Autor/Arquiteturas Propostas/Helpdesk 17/Notebooks/A) SA_BiLSTM___5.7005.ipynb"
```

## Status
Concluído. Artigo associado: ver [jidm-2024-remaining-time-prediction-dl](https://github.com/RonildoSilva/jidm-2024-remaining-time-prediction-dl) e [sbbd-2023-artigo](https://github.com/RonildoSilva/sbbd-2023-artigo).

## Autor
Ronildo Silva · ronildo.comp@gmail.com
