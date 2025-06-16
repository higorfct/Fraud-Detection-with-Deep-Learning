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

![image](https://github.com/user-attachments/assets/749d3058-a426-4586-b4e9-b8e6d5250290)

O modelo obteve uma acurácia de 79% na detecção de transações legítimas e fraudulentas.Para além da acurácia em si, as métricas de **precision** e **recall** ficaram equilibradas para ambas as classes, o que é crucial no contexto de detecção de fraudes, onde o custo financeiro dos erros é assimétrico.

Com **recall** de 80% para a **classe 1** (fraude), o modelo conseguiu identificar 8 em cada 10 transações fraudulentas, o que pode levar a uma redução considerável de perdas financeiras. Além disso, com **precision** de 80%, a maioria das transações sinalizadas como fraude realmente eram suspeitas, o que minimiza custos operacionais com falsas investigações.

Em resumo, os valores das métricas **precision** e **recall** indicam que o modelo tem boa capacidade preditiva de ajudar a reduzir custos operacionais com fraudes tanto em casos de falsos positivos (detectar como fraude uma transação legítima) quanto em casos de falsos negativos (detectar como legítima uma transação fraudulenta), o que é confirmado pelo valor do **F1-Score**.

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

