# Fase 4 – Resultados da Avaliação

A Fase 4 teve como objetivo executar a avaliação da qualidade dos requisitos do sistema **AgroMart**, com base no modelo **GQM (Goal-Question-Metric)** e nos critérios definidos nas Fases 2 e 3. A análise foi conduzida a partir de evidências coletadas diretamente do backlog e da documentação disponível, considerando os seguintes eixos:

---

## 4.1 Priorização de Requisitos (MoSCoW)

Foram analisadas 24 histórias de usuário do sistema. A distribuição entre as categorias MoSCoW foi:

- **Must**: 20 histórias (83,3%)  
- **Should**: 3 histórias (12,5%)  
- **Could / Won’t**: 0 histórias (0%)

Essa concentração excessiva na categoria **Must** evidencia uma priorização pouco balanceada.

**Julgamento**: **Crítico** — A ausência de equilíbrio entre as categorias limita a flexibilidade de planejamento e dificulta a identificação clara do MVP.

---

## 4.2 Justificativas dos Requisitos Must

Nenhuma das histórias classificadas como Must apresenta justificativa explícita de negócio ou critérios que sustentem sua essencialidade.

**Julgamento**: **Crítico** — A ausência de justificativas reduz a objetividade na definição de escopo e pode gerar sobrecarga no desenvolvimento.

---

## 4.3 Qualidade das Histórias de Usuário (Critérios INVEST)

Aplicou-se a técnica **INVEST** às 11 histórias atribuídas ao papel de Administrador (US16 a US26). Apenas **2 histórias** atenderam integralmente aos critérios: Independente, Negociável, Valiosa, Estimável, Pequena e Testável.

**Julgamento**: **Crítico** — A maioria das histórias apresenta problemas de granularidade e testabilidade, comprometendo a clareza e modularidade dos requisitos.

---

## 4.4 Qualidade dos Critérios de Aceitação (Critérios SMART)

Os critérios de aceitação foram avaliados com base nos princípios **SMART**. Nenhuma das histórias analisadas contempla integralmente os cinco critérios. O critério **Temporal** está ausente em todas.

**Julgamento**: **Crítico** — A ausência de critérios SMART dificulta a verificação objetiva dos requisitos e impacta negativamente os testes e validação.

---

## 4.5 Técnicas de Validação

A única técnica identificada foi a **validação informal**, com uso de checklist básico. Não foram observadas técnicas formais como revisões por pares.

**Julgamento**: **Crítico** — Técnicas informais não garantem a confiabilidade necessária nos critérios analisados (MoSCoW, INVEST, SMART).

---

## 4.6 Conclusão da Avaliação

Com base nas análises realizadas, todos os critérios avaliados apresentaram **nível crítico de qualidade**. Os principais problemas identificados foram:

- Priorização desequilibrada dos requisitos (MoSCoW)
- Ausência de justificativas para requisitos Must
- Fragilidade nas histórias de usuário (INVEST)
- Critérios de aceitação genéricos e pouco verificáveis (SMART)

---

## Recomendações

Recomenda-se à equipe de desenvolvimento:

1. **Revisar a priorização MoSCoW**, redistribuindo categorias com base em valor de negócio e viabilidade.
2. **Incluir justificativas para requisitos Must**, garantindo rastreabilidade e alinhamento com o escopo.
3. **Reformular as histórias de usuário**, assegurando aderência aos critérios INVEST.
4. **Aprimorar os critérios de aceitação**, com base nos princípios SMART.
5. **Adotar validação estruturada**, incluindo:
   - Checklists técnicos
   - Validação cruzada entre membros
   - Revisões formais com partes interessadas

---

### Exemplo de Checklist para Priorização MoSCoW

| Critério | Pontuação |
|----------|-----------|
| O projeto não é concluído sem essa US? | +1 |
| Não pode ser adiada? | +1 |
| Agrega valor de negócio? | +1 |

**Classificação**:

- 3 pontos → **MUST**
- 2 pontos → **SHOULD**
- 1 ponto  → **COULD**
- 0 pontos → **WON’T**

---

### Critérios Complementares de Esforço

| Critério | Pontuação |
|----------|-----------|
| A equipe já realizou algo semelhante? | +1 |
| Demanda menos de quatro horas? | +1 |
| Solução simples, sem necessidade de novas tecnologias? | +1 |
| Está alinhada aos padrões técnicos e arquiteturais? | +1 |

A combinação entre **valor de negócio** e **esforço** permite priorizar de forma mais clara o escopo do **MVP**, otimizando a entrega com base em critérios objetivos.

---
