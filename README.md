
# Análise Socioeconômica e Desempenho no ENEM 2020

Análise exploratória dos microdados do ENEM 2020, investigando como a renda familiar dos participantes se relaciona com a ausência nas provas e com o desempenho nas diferentes áreas do conhecimento.

## Sobre o projeto

O ENEM (Exame Nacional do Ensino Médio) é a principal porta de entrada para o ensino superior no Brasil. Este projeto usa os microdados oficiais de 2020 para investigar, de forma exploratória, o quanto a renda familiar declarada (variável `Q006`) está associada à evasão e ao desempenho dos participantes.

Todo o desenvolvimento está em um notebook Jupyter, usando **Python**, **Pandas** e **Matplotlib/Seaborn** para limpeza, análise e visualização dos dados.

## Perguntas de pesquisa

1. **Correlação entre Renda e Ausência** — A taxa de ausência é maior entre os participantes de faixas de renda mais baixas?
2. **O Teto de Desempenho** — Candidatos de faixas de renda mais altas apresentam, consistentemente, maiores notas em todas as áreas do conhecimento?
3. **A Redação como Equalizador** — A disparidade de notas entre as faixas de renda é menor na redação do que nas áreas de exatas?

## Principais achados

- **Ausência**: participantes das faixas de renda mais baixas (A e B) faltam bem mais — a taxa de ausência chega a ~60%, contra ~30% nas faixas de renda mais alta.
- **Desempenho**: a nota média sobe de forma consistente conforme a renda aumenta, em todas as 5 áreas do conhecimento.
- **Redação**: ao contrário do que se poderia esperar, a Redação é a área com a **maior** disparidade de notas entre faixas de renda (não a menor) — a diferença entre a faixa mais pobre e a mais rica passa de 200 pontos.

Os detalhes completos de cada análise, incluindo gráficos e discussão, estão no notebook.

## Estrutura do projeto

```
enem-data-dashboard/
├── dados/
│   ├── brutos/       # Microdados originais do INEP (não versionados, ver abaixo)
│   └── tratados/      # Dados tratados/exportados durante a análise
├── notebooks/
│   └── 01_exploracao_inicial.ipynb   # Análise principal
├── LICENSE
└── README.md
```

## Como rodar localmente

1. Clone o repositório:

   ```bash
   git clone https://github.com/CoderAugusto/enem-data-dashboard.git
   cd enem-data-dashboard
   ```
2. Crie e ative um ambiente virtual, e instale as dependências:

   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   pip install pandas numpy matplotlib seaborn jupyter
   ```
3. Baixe os microdados do ENEM 2020 no [portal do INEP](https://www.gov.br/inep/pt-br/acesso-a-informacao/dados-abertos/microdados/enem) e extraia o conteúdo em:

   ```
   dados/brutos/microdados_enem_2020/DADOS/MICRODADOS_ENEM_2020.csv
   ```
4. Abra o notebook e rode as células em ordem:

   ```bash
   jupyter notebook notebooks/01_exploracao_inicial.ipynb
   ```

## Fonte dos dados

Microdados do ENEM 2020, disponibilizados publicamente pelo [INEP](https://www.gov.br/inep/pt-br/acesso-a-informacao/dados-abertos/microdados/enem) (Instituto Nacional de Estudos e Pesquisas Educacionais Anísio Teixeira).

## Tecnologias utilizadas

- Python 3
- Pandas / NumPy
- Matplotlib / Seaborn
- Jupyter Notebook

## Licença

Este projeto está licenciado sob a licença MIT — veja o arquivo [LICENSE](LICENSE) para mais detalhes.
