# Projeto 5: Detecção de Fraudes

# 📊 Projeto: Detecção de Transações Fraudulentas

## 📝 Introdução

Neste trabalho, tem-se como principal objetivo **detectar transações suspeitas ou fraudulentas** para uma loja que atua tanto no comércio físico quanto online a fim de reduzir perdas financeiras para a instituição.  
Com essa abordagem, é possível apoiar o negócio na avaliação de riscos, aumentando a eficácia na detecção de fraudes enquanto se evita bloqueios desnecessários de transações legítimas.

---

## 📊 Dados

- Conjunto de Dados: `fraudes.csv`
- Quantidade de Registros: 3.784
- Quantidade de Atributos: 4
- Atributo-Alvo: `Class` (0 = Transação Válida, 1 = Transação Fraudulenta)
- Atributos previsores: `amount`(valor da transação), `time`(hora da transação) e `location`(localização da transação)

---

### Etapas realizadas:
- Importação das bibliotecas necessárias
- Carregamento do dataset
- Verificação da quantidade de registros e atributos
- Checagem de valores faltantes
- Pré-processamento (engenharia de atributos, normalização e divisão entre treino e teste)
- Aplicação de uma Rede Neural MLP para detecção de transações fraudulentas

---

## 🤖 Modelagem Preditiva

Algoritmo utilizado:
- **Rede Neural MLP (MLPClassifier)**

- Foi executado uma **tunagem de hiperparâmetros** (RandomizedSearchCV) para encontrar a combinação ótima.
- Os parâmetros otimizados incluem:
  - `hidden_layer_sizes`
  - `activation`
  - `solver`
  - `alpha`

---

## ✅ Resultados

# Interpretação das Métricas da Rede Neural MLP para Detecção de Fraudes

Este relatório apresenta as métricas de desempenho da rede neural MLP aplicada à detecção de fraudes em transações financeiras.

| Classe        | Precision | Recall | F1-score | Support |
|---------------|-----------|--------|----------|---------|
| 0             | 0.88      | 0.81   | 0.84     | 363     |
| 1             | 0.84      | 0.90   | 0.87     | 394     |
| **Accuracy**  |           |        | **0.85** | 757     |
| **Macro avg** | 0.86      | 0.85   | 0.85     | 757     |
| **Weighted avg** | 0.86   | 0.85   | 0.85     | 757     |

## Análise Geral

- A **acurácia geral** do modelo é de 85%, indicando que ele classificou corretamente 85% das transações.
- O **recall da classe fraude (90%)** é alto, mostrando que o modelo consegue detectar a maioria das fraudes, minimizando falsos negativos.
- A **precisão da classe fraude (84%)** indica que a maioria das transações classificadas como fraude são realmente fraudulentas, reduzindo falsos positivos.
- Para a classe não fraude, o modelo apresenta precisão de 88% e recall de 81%, o que indica que uma pequena parte das transações legítimas pode ser sinalizada como fraude (falsos positivos).
- O modelo apresenta um bom equilíbrio entre capturar fraudes com sensibilidade e evitar falsos alarmes.

Essas métricas indicam que o modelo é eficaz para uso em sistemas de prevenção a fraudes, garantindo alta detecção de casos fraudulentos e mantendo os erros dentro de níveis aceitáveis.


---

## 💰 Impacto Financeiro Potencial 

O modelo gerou impactos financeiros relevantes na detecção de fraudes, conforme detalhado abaixo:

- **Custo de Falsos Positivos:** R$ 180.432,57  
  (Valor gasto devido a transações legítimas incorretamente classificadas como fraude)

- **Economia de Verdadeiros Positivos:** R$ 923.082,56  
  (Valor economizado ao detectar corretamente transações fraudulentas)

- **Impacto Monetário Líquido:** R$ 742.649,99  
  (Economia total após considerar os custos gerados pelos falsos positivos)

Esses números mostram que o modelo contribui para uma economia financeira significativa ao reduzir perdas com fraudes, mesmo levando em conta os custos dos falsos alarmes.



---

## 🛠️ Ferramentas Utilizadas

- **Python** – Linguagem principal
- **Pandas** – Manipulação e análise de dados
- **Matplotlib / Seaborn** – Visualização gráfica
- **Scikit-learn** – Modelagem preditiva e métricas
- **Jupyter Notebook** – Ambiente de desenvolvimento

---

## 🧠 Conclusão

A **Rede Neural Artificial (MLP)** mostrou que é capaz de:

- Detectar transações fraudulentas com **eficácia**, enquanto mantém um **número relativamente baixo de falsos positivos**.
- A avaliação revela que o modelo é particularmente robusto para um problema onde o conjunto de dados é **altamente desbalanceado**.
- A detecção automática permitirá às empresas prevenir fraudes em tempo real, aumentando a **segunrança** nas transações financeiras.

---

## 🔄 Próximos Passos

- Implementar o modelo em um pipeline de produção junto às transações em tempo real.
- Realizar um **fine-tuning** dos parâmetros para obter ainda maior recall.
- Experimentar outros algoritmos (Gradient Boosting, LightGBM, XGBoost) para melhoria de desempenho.

---

🧑‍💻 **Autor e Contato**

**Higor Roberto Coutinho Caetano**  
**LinkedIn**: [https://www.linkedin.com/in/higor-caetano-049521136/](https://www.linkedin.com/in/higor-caetano-049521136/)  
**E-mail**: higorfct@gmail.com

