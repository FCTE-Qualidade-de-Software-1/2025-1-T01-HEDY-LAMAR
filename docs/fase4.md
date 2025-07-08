# Fase 4 – Resultados da Avaliação

A Fase 4 teve como objetivo executar a avaliação da qualidade dos requisitos do sistema AgroMart, com base no modelo GQM (Goal-Question-Metric) e nos critérios definidos nas Fases 2 e 3. A análise foi conduzida a partir de evidências coletadas diretamente do backlog e da documentação disponível, considerando os seguintes eixos:

---

## 4.1 Priorização de Requisitos (MoSCoW)

Para avaliar a priorização MoSCoW, foram abordadas três questões principais:

**Q1**: A classificação de prioridade do RF faz sentido considerando o valor que esse recurso oferece ao usuário?

- **Análise de Dados:** A avaliação de alguns requisitos-chave indicou que a sua classificação de prioridade na documentação existente pode não refletir o valor percebido pelos usuários finais.

| Requisito | Descrição                                                      | Categoria     |
| :-------- | :------------------------------------------------------------- | :-------------- |
| RF6       | O co-agricultor deve ser capaz de escolher o método de pagamento | *Could* |
| RF8       | O co-agricultor deve ser capaz de entrar em contato com o Administrador | *Won't* have |
| RNF10     | O co-agricultor deve saber os itens que virão na cesta da semana | *Could* |

- **Discussão**: A hipótese inicial de que a priorização de RF6, RF8 e RNF10 (classificados como *Could*/*Won't*) pode não refletir o real valor percebido pelos usuários foi confirmada pela observação de que funcionalidades básicas ou de comunicação direta foram subpriorizadas. Caso os usuários atribuam maior importância a esses requisitos, suas prioridades deverão ser revistas para garantir alinhamento entre valor de negócio e planejamento de entrega.

**Q2**: A distribuição dos requisitos entre as categorias MoSCoW está balanceada?

- **Análise de Dados:** Foram analisadas 24 histórias de usuário do sistema. A distribuição entre as categorias MoSCoW foi:
      - *Must*: 20 histórias (83,3%)
      - *Should*: 3 histórias (12,5%)
      - *Could* / *Won’t*: 0 histórias (0%)
  
- **Discussão**: Esta concentração excessiva na categoria *Must* (83,3%) evidencia uma priorização pouco balanceada, o que pode comprometer o foco estratégico na entrega de valor. A ausência de requisitos na categoria *Could*/*Won't* e a baixa representatividade de *Should* indicam uma falha na diferenciação de prioridades.

- **Observação**: O requisito RF-9 está ausente na tabela de requisitos analisada, o que pode indicar que foi omitido ou removido. É importante revisar a numeração para garantir a consistência e rastreabilidade dos requisitos.

**Q3**: Os requisitos "*Must*" estão claramente justificados como essenciais para o funcionamento mínimo do sistema?

- **Análise de Dados:** Não. Nenhuma das histórias classificadas como *Must* apresenta justificativa explícita de negócio ou critérios que sustentem sua essencialidade.

- **Discussão**: A ausência de justificativas compromete a rastreabilidade e dificulta a validação de sua real prioridade, tornando a definição de escopo subjetiva.

Julgamento Global da Priorização de Requisitos (MoSCoW): Crítico — A ausência de equilíbrio entre as categorias limita a flexibilidade de planejamento e dificulta a identificação clara do MVP. A falta de justificativas para os requisitos *Must* agrava este problema.

## 4.2 Justificativas dos Requisitos *Must*

- **Análise de Dados**: Esta seção já foi detalhada na análise de Q3 dentro da Priorização de Requisitos (4.1). Para reforçar, constatou-se que nenhuma das histórias classificadas como *Must* apresenta justificativa explícita de negócio ou critérios que sustentem sua essencialidade.

Julgamento Global das Justificativas dos Requisitos *Must*: Crítico — A ausência de justificativas reduz a objetividade na definição de escopo e pode gerar sobrecarga no desenvolvimento.

## 4.3 Qualidade das Histórias de Usuário (Critérios INVEST)

Para avaliar a qualidade das Histórias de Usuário, foi abordada a seguinte questão:

**Q1**: As histórias de usuário demonstram uma abstração do requisito permitindo analisar como uma funcionalidade que permeia a utilização do produto pelo usuário?

- **Análise de Dados**: Aplicou-se a técnica INVEST às 11 histórias atribuídas ao papel de Administrador (US16 a US26). Os resultados da análise de aderência foram:

### Histórias de Usuário - Administrador

- ***Login***
    - US16: Realizar *login* no Strapi
    - US17: Realizar *login* no Aplicativo
- **Instalar**
    - US18: Possuir um tutorial
- **Strapi - Gerenciar**
    - US19: Interagir com Produtos
    - US20: Interagir com Planos
    - US21: Interagir com Cestas
    - US22: Interagir com Co-agricultor
    - US23: Interagir com Lojas
    - US24: Criar Notificações
    - US25: Interagir com Pedidos
    - US26: Visualizar endereços

A análise de aderência aos critérios INVEST para essas histórias de usuário resultou na seguinte tabela:

| US's | Independente | Negociável | Valiosa | Estimável | Pequena | Testável |
|-------|-------------|------------|---------|-----------|---------|----------|
| US16  | ✅           | ✅          | ✅       | ✅         | ✅       | ✅        |
| US17  | ✅           | ✅          | ✅       | ✅         | ✅       | ✅        |
| US18  | ✅           | ✅          | ✅       | ❌         | ✅       | ❌        |
| US19  | ❌           | ✅          | ✅       | ✅         | ❌       | ✅        |
| US20  | ❌           | ✅          | ✅       | ✅         | ❌       | ✅        |
| US21  | ❌           | ✅          | ✅       | ✅         | ❌       | ✅        |
| US22  | ❌           | ✅          | ✅       | ✅         | ❌       | ✅        |
| US23  | ✅           | ✅          | ✅       | ✅         | ❌       | ❌        |
| US24  | ✅           | ✅          | ✅       | ✅         | ✅       | ✅        |
| US25  | ❌           | ✅          | ✅       | ✅         | ❌       | ❌        |
| US26  | ✅           | ✅          | ✅       | ✅         | ✅       | ✅        |

- **Discussão**: Apenas 2 histórias (US16 e US17) atenderam integralmente a todos os critérios INVEST. Observa-se uma recorrência de falhas nos critérios "Independente", "Pequena" e "Testável". A hipótese inicial de que várias US's não atenderiam a esses critérios foi confirmada.

Julgamento Global da Qualidade das Histórias de Usuário (Critérios INVEST): Crítico — A maioria das histórias apresenta problemas de granularidade e testabilidade, comprometendo a clareza e modularidade dos requisitos.

## 4.4 Qualidade dos Critérios de Aceitação (Critérios SMART)

Para avaliar a clareza dos Critérios de Aceitação, foi abordada a seguinte questão:

**Q2**: Os critérios de aceitação das histórias de usuário são claros, objetivos e testáveis garantindo métricas que sustentam a implementação e verificação?

- **Análise de Dados**: Os critérios de aceitação foram avaliados com base nos princípios SMART.

### Exemplos de critérios de aceitação:

- **US16:** Deve efetuar o *login*.
- **US17:** Deve efetuar o *login*. Deve ter o código da CSA.
- **US18:** Tutorial disponível na documentação. Ter passo a passo. Ser de fácil compreensão.
- **US19:** Deve estar logado. Deve ser o responsável pela CSA. Deve ser capaz de adicionar, editar e visualizar produtos.
- **US20 a US26:** Seguem o mesmo padrão: *login*, responsabilidade pela CSA e ações específicas.

A análise de aderência aos princípios SMART resultou na seguinte tabela:

| US's | Específico | Mensurável | Alcançável | Relevante | Temporal |
|-------|-----------|------------|------------|-----------|----------|
| US16  | ✅         | ✅          | ✅          | ✅         | ❌        |
| US17  | ✅         | ✅          | ❓          | ✅         | ❌        |
| US18  | ✅         | ✅          | ✅          | ✅         | ❌        |
| US19  | ✅         | ✅          | ❓          | ✅         | ❌        |
| US20  | ✅         | ✅          | ❓          | ✅         | ❌        |
| US21  | ✅         | ✅          | ❓          | ✅         | ❌        |
| US22  | ✅         | ✅          | ❓          | ✅         | ❌        |
| US23  | ✅         | ✅          | ❓          | ✅         | ❌        |
| US24  | ✅         | ❓          | ❓          | ✅         | ❌        |
| US25  | ✅         | ❓          | ❓          | ✅         | ❌        |
| US26  | ✅         | ❓          | ❓          | ✅         | ❌        |

- **Discussão**: Nenhuma das histórias analisadas contempla integralmente os cinco critérios SMART, especialmente o critério Temporal, que está ausente em todas as avaliações. Além disso, há muitas indefinições ('❓') em "Mensurável" e "Alcançável". Isso valida a hipótese de que os critérios de aceitação não são suficientemente claros, objetivos e testáveis.

Julgamento Global da Qualidade dos Critérios de Aceitação (Critérios SMART): Crítico — A ausência de critérios SMART dificulta a verificação objetiva dos requisitos e impacta negativamente os testes e validação.

## 4.5 Técnicas de Validação

Para avaliar a suficiência das técnicas de validação, foi abordada a seguinte questão:

**Q3**: As técnicas de validação utilizadas no projeto são suficientes sob a perspectiva dos processos da Engenharia de Requisitos?

- **Análise de Dados**: Atualmente, a única técnica de validação identificada na documentação é a validação informal, com uso de checklist básico. Não foram observadas técnicas formais como revisões por pares ou a aplicação sistemática de critérios como INVEST e SMART dentro do processo de validação.

- **Discussão**: A hipótese de que a validação informal é insuficiente para garantir a qualidade dos requisitos foi confirmada. Embora haja um checklist, ele é limitado e genérico, não utilizando modelos como INVEST ou SMART para uma avaliação mais criteriosa. Técnicas formais poderiam minimizar erros antes da implementação e melhorar a rastreabilidade e consistência.

Julgamento Global das Técnicas de Validação: Crítico — A validação informal, sem uma estrutura robusta ou uso de abordagens formais, não garante a confiabilidade necessária na qualidade dos requisitos analisados (MoSCoW, INVEST, SMART).

## 4.6 Conclusão da Avaliação

Com base nas análises realizadas, conclui-se que todos os critérios avaliados apresentaram nível crítico de qualidade. Os principais problemas identificados foram:

- Priorização desequilibrada dos requisitos (MoSCoW)
- Ausência de justificativas para requisitos *Must*
- Fragilidade nas histórias de usuário (INVEST)
- Critérios de aceitação genéricos e pouco verificáveis (SMART)
- Dependência exclusiva de técnicas de validação informal

## Recomendações

Recomenda-se à equipe de desenvolvimento:

1. Revisar a priorização MoSCoW, redistribuindo categorias com base em valor de negócio e viabilidade para criar um MVP mais claro.
2. Incluir justificativas para requisitos *Must*, garantindo rastreabilidade e alinhamento com o escopo e facilitando a compreensão da essencialidade.
3. Reformular as histórias de usuário, assegurando aderência aos critérios INVEST, com foco em granularidade, independência e testabilidade.
4. Aprimorar os critérios de aceitação, com base nos princípios SMART (Específico, Mensurável, Alcançável, Relevante, Temporal), especialmente incluindo o aspecto temporal.
5. Adotar validação estruturada, incluindo:
      1. Checklists técnicos mais robustos (baseados em INVEST e SMART).
      2. Validação cruzada entre membros da equipe para identificar vieses e erros.
      3. Revisões formais com partes interessadas para garantir o alinhamento com as expectativas do negócio.

## 4.7 Ações de melhoria

Com base nos julgamentos críticos apresentados nas seções anteriores, especialmente a priorização desequilibrada de requisitos (MoSCoW) e a ausência de justificativas para requisitos *Must*, a equipe selecionou e implementou uma ação de melhoria focada em aprimorar o processo de priorização e definição de escopo do AgroMart.

**Ação de Melhoria Escolhida:** Proposição de um método aprimorado para Priorização de Requisitos, combinando a técnica MoSCoW com critérios complementares de esforço. Esta ação se materializa na disponibilização de um template técnico e um guia de classificação para auxiliar na tomada de decisão de priorização. 

**Justificativa**: A análise da Fase 4 revelou que a alta concentração de requisitos "*Must*" (83,3%) e a completa ausência de justificativas explícitas comprometem a flexibilidade e a objetividade da priorização. Para endereçar esses problemas, a proposição de um método mais estruturado e objetivo, que integra tanto o valor de negócio quanto o esforço necessário, visa garantir uma seleção mais equilibrada e estratégica das funcionalidades, auxiliando na identificação clara do Produto Mínimo Viável (MVP).

### Implementação: 

Foi desenvolvido um conjunto de guidelines e um template técnico para a priorização de requisitos, que detalha:

#### Exemplo de Checklist para Priorização MoSCoW

| Critério | Pontuação |
|----------|-----------|
| O projeto não é concluído sem essa US? | +1 |
| Não pode ser adiada? | +1 |
| Agrega valor de negócio? | +1 |

#### Classificação:

- 3 pontos → *MUST*
- 2 pontos → SHOULD
- 1 ponto  → COULD
- 0 pontos → WON’T

#### Critérios Complementares de Esforço

| Critério | Pontuação |
|----------|-----------|
| A equipe já realizou algo semelhante? | +1 |
| Demanda menos de quatro horas? | +1 |
| Solução simples, sem necessidade de novas tecnologias? | +1 |
| Está alinhada aos padrões técnicos e arquiteturais? | +1 |

A combinação entre valor de negócio e esforço permite priorizar de forma mais clara o escopo do MVP, otimizando a entrega com base em critérios objetivos.

## Tabela de contribuição

| Matrícula   | Nome completo                          | Contribuição (%) |
|-------------|--------------------------------------|------------------|
| 221022462   | [Arthur da Silveira Sousa](https://github.com/Tutzs)           | 16,6             |
| 221022515   | [Danilo Naves do Nascimento](https://github.com/DaniloNavesS)  | 16,6             |
| 180100271   | [Emivalto da Costa Tavares Junior](https://github.com/EmivaltoJrr) | 16,6         |
| 222014859   | [Ian Costa Guimarães](https://github.com/iancostag)            | 16,6             |
| 200020323   | [Jefferson Sena Oliveira](https://github.com/JeffersonSenaa)   | 16,6             |
| 211062016   | [José André Rabelo Rocha](https://github.com/joseandre25)      | 16,6             |
