# Análise de Indicadores de Fake News em Redes Sociais

Projeto técnico de TCC: classificação de fake news no corpus FakeRecogna (Python) e visualização comparativa dos resultados (Power BI).

## Estrutura do projeto

```
TCC_AnaliseFakeNews/
├── notebooks/    Os 4 notebooks Jupyter, em ordem de execução (Fase 1 → Fase 4)
├── dados/        CSVs de entrada e checkpoints gerados entre as fases
├── figuras/      Imagens (.png, 300 dpi) prontas para o artigo escrito
└── requirements.txt
```

## Ordem de execução

1. `notebooks/Fase1_Setup_Exploracao_FakeRecogna.ipynb` — carrega o FakeRecogna, explora a estrutura, salva `dados/fakerecogna_bruto.csv`
2. `notebooks/Fase2_Limpeza_Vazamento_Classificador.ipynb` — limpeza, checagem de vazamento de dados, treina os classificadores, salva `dados/resultados_classificacao.csv`
3. `notebooks/Fase3_Figuras_para_o_Artigo.ipynb` — gera a figura de acurácia por categoria
4. `notebooks/Fase4_Identificando_Agencias_FactChecking.ipynb` — identifica a agência de fact-checking de origem de cada notícia, salva `dados/fakerecogna_com_fonte.csv`

Cada notebook espera ser executado de dentro da pasta `notebooks/` (os caminhos usam `../dados/` e `../figuras/`).

## Setup (Windows + VS Code)

```
python -m venv venv
.\venv\Scripts\Activate.ps1
pip install -r requirements.txt
```

## Uso complementar: Power BI

O arquivo `.pbix` do dashboard interativo (usado na apresentação oral) fica fora deste projeto Python — ele lê `dados/resultados_classificacao.csv` diretamente.
