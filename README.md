# 📊 Análise Exploratória de Dados — Titanic & Eleições Brasileiras

> Trabalho acadêmico desenvolvido para a disciplina de **Estatística**  
> MBA em Ciência de Dados

---

## 📋 Descrição do Projeto

Este projeto realiza uma **Análise Exploratória de Dados (EDA)** sobre dois conjuntos de dados distintos:

- **Titanic** — dados históricos dos passageiros do RMS Titanic, explorando perfil demográfico, classe social e sobrevivência.
- **Eleições Brasileiras** — dados de candidatos por estado, cruzando financiamento de campanha (`Dinheiro`) e resultado nas urnas (`Votos`).

O objetivo é aplicar técnicas estatísticas descritivas e de visualização para extrair insights relevantes, identificar padrões e comunicar achados de forma clara e fundamentada.

---

## 🗂️ Estrutura do Projeto

```
.
├── projeto_EDA_Dalton.ipynb    # Notebook principal com toda a análise
├── titanic.csv                 # Dataset do Titanic
├── eleicoes.csv                # Dataset das Eleições Brasileiras
└── README.md
```

---

## 📦 Datasets

### 🚢 Titanic (`titanic.csv`)

| Coluna | Tipo | Descrição |
|---|---|---|
| `Survived` | Qualitativa (nominal) | 0 = não sobreviveu, 1 = sobreviveu |
| `Pclass` | Qualitativa (ordinal) | Classe do bilhete (1ª, 2ª ou 3ª) |
| `Name` | Qualitativa (nominal) | Nome do passageiro |
| `Sex` | Qualitativa (nominal) | Sexo do passageiro |
| `Age` | Quantitativa (contínua) | Idade em anos |
| `Siblings/Spouses Aboard` | Quantitativa (discreta) | Nº de irmãos/cônjuges a bordo |
| `Parents/Children Aboard` | Quantitativa (discreta) | Nº de pais/filhos a bordo |
| `Fare` | Quantitativa (contínua) | Valor da tarifa paga |

### 🗳️ Eleições (`eleicoes.csv`)

| Coluna | Tipo | Descrição |
|---|---|---|
| `Estado` | Qualitativa (nominal) | Unidade Federativa (UF) |
| `NumeroCand` | Qualitativa (nominal) | Número do candidato |
| `Dinheiro` | Quantitativa (contínua) | Valor arrecadado em campanha (R$) |
| `Votos` | Quantitativa (discreta) | Total de votos recebidos |

---

## 🔬 Análises Realizadas

### Dataset 1 — Titanic

| # | Análise |
|---|---|
| 1 | Identificação e classificação das variáveis (qualitativas × quantitativas) |
| 2 | Gráficos de barras e pizza para `Sex`, `Pclass` e `Survived` |
| 3 | Medidas de tendência central e dispersão para `Age` e `Fare` (média, mediana, desvio padrão, mín., máx., percentis 10 e 90) |
| 4 | Histograma da variável `Age` com linhas de média e mediana |
| 5 | Gráfico de dispersão `Age × Fare` e correlação de Pearson |

### Dataset 2 — Eleições

| # | Análise |
|---|---|
| 1 | Histogramas de `Votos` e `Dinheiro` para 3 estados (CE, SP e RS) |
| 2 | Gráficos de dispersão `Dinheiro × Votos` e correlação de Pearson por estado |
| 3 | Tabela de correlação de Pearson (`Dinheiro × Votos`) para todos os estados do Brasil |
| 4 | Tabela-resumo estatístico por estado: média, mediana, desvio padrão, mín., máx., Q1 e Q3 |

---

## 🛠️ Tecnologias Utilizadas

| Biblioteca | Versão | Uso |
|---|---|---|
| `Python` | 3.13+ | Linguagem base |
| `pandas` | — | Manipulação e agregação de dados |
| `matplotlib` | — | Visualizações (histogramas, barras, pizza, dispersão) |
| `numpy` | — | Suporte a operações numéricas |
| `Jupyter Notebook` | — | Ambiente de desenvolvimento interativo |

---

## ▶️ Como Executar

1. **Clone ou baixe** os arquivos do projeto.

2. **Instale as dependências** (caso necessário):

```bash
pip install pandas matplotlib numpy jupyter
```

3. **Coloque os datasets** nas pastas corretas:
   - `titanic.csv` na raiz do projeto
   - `eleicoes.csv` dentro da pasta `datasets/`

4. **Inicie o Jupyter Notebook**:

```bash
jupyter notebook projeto_EDA_Dalton.ipynb
```

5. Execute as células em ordem (`Kernel > Restart & Run All`).

---

## 💡 Principais Achados

### Titanic
- Passageiros do sexo masculino representavam cerca de **65% do total**, mas a taxa de sobrevivência feminina foi significativamente maior.
- A **3ª classe** concentrava mais passageiros do que 1ª e 2ª juntas, com menor taxa de sobrevivência.
- A **correlação entre idade e tarifa é fraca**, indicando que o valor pago era determinado principalmente pela classe social.
- A distribuição de idades é aproximadamente simétrica, com concentração entre **20 e 40 anos**.

### Eleições Brasileiras
- Tanto votos quanto financiamento de campanha seguem distribuições com **forte assimetria à direita** em todos os estados analisados.
- Existe uma **correlação positiva moderada a forte** entre dinheiro arrecadado e votos obtidos, consistente em todo o país.
- A desigualdade de recursos é expressiva: a maioria dos candidatos arrecada e recebe poucos votos, enquanto uma minoria concentra a maior parte dos recursos e da votação.

---

## 📁 Observações

- Os gráficos foram padronizados com estilo consistente (grade suave, sem bordas desnecessárias, paleta de cores intencional).
- Cada análise é acompanhada de um comentário interpretativo diretamente no notebook.
- Os estados escolhidos para análise individual foram **CE (Ceará)**, **SP (São Paulo)** e **RS (Rio Grande do Sul)**.

---

## 👨‍🎓 Informações Acadêmicas

| | |
|---|---|
| **Curso** | MBA em Ciência de Dados |
| **Disciplina** | Estatística Básica|
| **Tipo** | Trabalho Prático — Análise Exploratória de Dados |