# 📊 Pairs Trading com Ações Brasileiras usando Clustering

Este projeto aplica técnicas de **clustering** e **testes de cointegração** para identificar **pares de ações brasileiras** que se movimentam de forma semelhante ao longo do tempo, com o objetivo de aplicar estratégias de **pairs trading**.

---

## 🧠 O que é Pairs Trading?

É uma estratégia de investimento onde você compra uma ação e vende outra correlacionada. Quando os preços se **desalinharem temporariamente**, espera-se que voltem ao padrão histórico — e essa diferença gera **oportunidade de lucro**.

Imagine dois ativos "parças de mercado": se um se afasta, a estratégia aposta que eles vão se reconciliar logo. 💸

---

## 🔧 O que o projeto faz?

- Coleta e organiza os dados de preços de ações brasileiras.
- Usa **algoritmos de clustering** (K-Means, Hierarchical e Affinity Propagation) para agrupar ações com padrões semelhantes.
- Aplica testes de **cointegração** (ADF e Johansen) para identificar pares com relação estável de longo prazo.
- Retorna uma lista de pares com alto potencial para uso em estratégias de *trading*.

---

## 📚 Técnicas e ferramentas usadas

- `Python`
- `pandas`, `numpy`, `matplotlib`, `scipy`, `statsmodels`
- Algoritmos de clustering:
  - K-Means
  - Hierarchical Clustering (com dendrogramas)
  - Affinity Propagation
- Testes estatísticos:
  - **ADF (Augmented Dickey-Fuller)**
  - **Johansen Test**

---

## 📈 Exemplo de uso

```python
# Exemplo: rodar clustering e obter pares cointegrados
from clustering_pairs import executar_clustering, testar_cointegracao

clusters = executar_clustering(dados_ajustados)
pares = testar_cointegracao(clusters)
