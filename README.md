# 🧪 Sifit — QA Manual

Testes manuais do **Sifit**, sistema de gestão de academias, cobrindo consulta, cadastro, edição e exclusão nas principais áreas: clientes, matrículas, planos, check-in, avaliações físicas, treinamento, financeiro, comercial, gestão e configurações.

## 📊 Números

| | |
| --- | --- |
| Requisitos funcionais mapeados | **31** |
| Cenários de teste | **98** |
| Bugs encontrados | **16** |

## 📁 Documentação

| Documento | Conteúdo |
| --- | --- |
| [`Sifit/1-Analise de requisitos.md`](Sifit/1-Analise%20de%20requisitos.md) | Requisitos funcionais (RF01–RF31), um por tela/submódulo |
| [`Sifit/2-plano de testes.md`](Sifit/2-plano%20de%20testes.md) | Escopo, técnicas, cronograma e critérios de aceitação |
| [`Sifit/3-Relatorio-de-Bugs.md`](Sifit/3-Relatorio-de-Bugs.md) | Falhas encontradas, com passos de reprodução e evidências |
| [`Sifit/4- Relatorio dos testes.md`](Sifit/4-%20Relatorio%20dos%20testes.md) | Resumo da execução, cobertura por módulo e conclusão |
| [`Sifit/Cenarios de testes/`](Sifit/Cenarios%20de%20testes) | Casos de teste em BDD (Gherkin), um arquivo por RF |

## 🔎 Principal achado

Quatro fluxos centrais de **cadastro** (Matrícula, Plano, Avaliação Física e Ficha de Treino) falham com erro do servidor (HTTP 400/500), um padrão sistêmico e não bugs isolados — detalhado no relatório de execução.

## 🧪 Metodologia

Testes positivos, negativos e exploratórios, com registros de teste identificados pelo prefixo `QA_` para não afetar dados reais da academia.
