# Projeto código morto, gráficos para observação de dados


## RQ1 — Extensão e distribuição  
**H1:** código morto compõe 5%–20% das LOC, concentrando-se em módulos pouco atualizados.  

Os resultados mostram que a média de código morto por repositório varia entre cerca de **0,6% (JavaScript)** e **16% (Python)**, com **Java (12%)** e **Go (8%)** também dentro da faixa proposta. Isso confirma parcialmente a hipótese — a maioria das linguagens tem valores médios dentro ou próximos do intervalo de 5% a 20%. Além disso, a mediana de 0% nos módulos indica que o código morto tende a se concentrar em **apenas parte dos módulos**, não de forma uniforme.  

**Conclusão:** H1 **parcialmente confirmada**.

---

## RQ2 — Linguagem predominante  
**H2:** linguagens dinâmicas (JS/TS, Python) exibem maiores proporções que linguagens estáticas (Java, Go).  

Os dados mostram que **Python** apresenta a maior média de código morto (≈16%), enquanto **JavaScript** e **TypeScript** têm percentuais muito baixos (≈0,6% e 1,5%). Já **Java** (12%) e **Go** (8%) — linguagens estáticas — têm valores moderados. Assim, **apenas Python** reforça a hipótese; JS e TS, apesar de dinâmicas, exibem menos código morto.  

**Conclusão:** H2 **não confirmada** — a relação entre tipo de linguagem e proporção de código morto não é consistente.

---

## RQ3 — Popularidade  
**H3:** projetos mais populares (mais stars/forks) apresentam menor proporção de código morto.  

As correlações de Spearman entre “dead_percent” e popularidade (stars/forks) são **negativas em quase todas as linguagens**, embora **fracas** e na maioria **não significativas** estatisticamente (p > 0.05). Isso sugere uma tendência leve, mas sem força estatística, de que repositórios mais populares têm menos código morto.  

**Conclusão:** H3 **fracamente suportada**, mas não confirmada de forma robusta.

---

## RQ4 — Impactos  
**H4:** maior % de código morto implica em tempos de build/teste mais longos e mais bugs/issues.  

As correlações entre código morto e tempo de CI são **fracas ou inexistentes** em todas as linguagens (rho próximo de 0). Já a correlação entre código morto e densidade de bugs é **positiva e significativa** para **Java, Python, Go e TypeScript**, indicando que repositórios com mais código morto tendem a ter **mais defeitos**.  

**Conclusão:** H4 **parcialmente confirmada** — o código morto parece aumentar a propensão a bugs, mas não afeta significativamente o tempo de CI.
