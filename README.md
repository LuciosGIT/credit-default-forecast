# Previsão de Pagamento de Empréstimos com Decision Trees e Random Forest

![LendingClub Logo](/lendingclub.jpeg)

Este projeto tem como objetivo construir modelos de machine learning para prever se um mutuário pagou integralmente seu empréstimo com base em dados financeiros históricos. Para isso, utilizamos os algoritmos **Decision Tree** e **Random Forest**, modelos baseados em árvores de decisão amplamente usados em problemas de classificação.

## Dataset

Os dados utilizados neste projeto são provenientes do LendingClub, uma plataforma de empréstimos peer-to-peer. O dataset abrange empréstimos concedidos entre 2007 e 2010 e foi obtido do Kaggle:  
[https://www.kaggle.com/datasets/sarahvch/predicting-who-pays-back-loans](https://www.kaggle.com/datasets/sarahvch/predicting-who-pays-back-loans)

### Descrição dos Atributos

- **credit.policy**: Indicador se o empréstimo foi concedido segundo a política de crédito da empresa (1 = sim, 0 = não).
- **purpose**: Finalidade do empréstimo (ex: carro, educação, dívidas, etc).
- **int.rate**: Taxa de juros anual do empréstimo.
- **installment**: Valor mensal da parcela a ser paga.
- **log.annual.inc**: Logaritmo da renda anual do mutuário.
- **dti**: Dívida em relação à renda (Debt-to-Income Ratio).
- **fico**: Score de crédito FICO do mutuário.
- **days.with.cr.line**: Número de dias que o mutuário tem uma linha de crédito aberta.
- **revol.bal**: Saldo rotativo do cartão de crédito.
- **revol.util**: Utilização do crédito rotativo (percentual do limite de crédito utilizado).

## Metodologia

- **Pré-processamento**: Tratamento de dados com pandas, codificação de variáveis categóricas e normalização quando aplicável.
- **Balanceamento das classes**: Como o dataset apresenta desbalanceamento entre mutuários que pagaram e que não pagaram integralmente, foram aplicadas técnicas de balanceamento para melhorar a performance do modelo.
- **Modelagem**: Treinei modelos de Decision Tree e Random Forest para classificação binária.
- **Otimização de hiperparâmetros**: Utilizei algoritmos de otimização como Grid Search, Randomized Search e Bayesian Search para encontrar a melhor combinação de parâmetros para cada modelo.
- **Avaliação**: O desempenho dos modelos foi avaliado por métricas como acurácia, precisão, recall, F1-score e matriz de confusão.

## Resultados

Os modelos apresentaram bom desempenho na previsão do pagamento integral dos empréstimos, com a Random Forest geralmente superando a Decision Tree simples após a otimização dos hiperparâmetros.  
No entanto, o modelo de Random Forest não apresentou um recall muito satisfatório para a classe 0 (mutuários que **não pagaram integralmente**), indicando que ainda há dificuldades em identificar corretamente esses casos.

Como próximo passo, planeja-se aplicar técnicas de **feature engineering** para extrair informações adicionais dos dados e, assim, melhorar ainda mais a capacidade preditiva do modelo.

## Como usar

```bash
# Clone o repositório
git clone https://github.com/seu-usuario/seu-repositorio.git
cd seu-repositorio

# Crie e ative um ambiente virtual (opcional, mas recomendado)
python -m venv venv
source venv/bin/activate  # Linux/macOS
venv\Scripts\activate     # Windows

# Instale as dependências
pip install -r requirements.txt

# Execute o notebook ou script principal
jupyter notebook    # ou python main.py, dependendo do seu projeto
```

Qualquer dúvida, fique à vontade para entrar em contato!

