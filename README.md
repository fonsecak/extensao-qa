# Sifit: Testes Funcionais Manuais

Projeto de garantia de qualidade desenvolvido na disciplina de Extensão em Qualidade de Software. O trabalho avalia o Sifit, sistema de gestão de academias, por meio de testes funcionais manuais que cobrem consulta, cadastro, edição e exclusão nos módulos de clientes, matrículas, planos, check-in, avaliações físicas, treinamento, financeiro, comercial, gestão e configurações.

## Visão geral

| Item | Descrição |
| --- | --- |
| Sistema avaliado | Sifit, sistema de gestão de academias |
| Tipo de teste | Funcional manual |
| Ambiente | Alfa ([sifitalfa.centrion.com.br](https://sifitalfa.centrion.com.br)) |
| Período de execução | 13/10/2026 a 18/11/2026 |
| Plataforma | Windows 11 e Google Chrome |
| Perfil utilizado | Administrativo |

## Resultados

| Indicador | Total |
| --- | :---: |
| Requisitos funcionais mapeados | **31** |
| Casos de teste executados | **98** |
| Casos com falha | **16** |
| Bugs registrados | **16** |

### Principal achado

Quatro fluxos centrais de cadastro (Matrícula, Plano, Avaliação Física e Ficha de Treino) falham com erro do servidor (HTTP 400 e 500). Trata-se de um padrão sistêmico, e não de falhas isoladas, com impacto direto nas operações mais frequentes da academia. Os quatro defeitos foram classificados com severidade alta e devem ser priorizados antes da liberação do sistema para uso real.

As demais falhas se concentram em validação insuficiente de dados, divergência entre o dado cadastrado e o dado exibido, mensagens de erro que não refletem o resultado da operação e exibição de credenciais sem mascaramento na tela de Configurações.

## Escopo

**Incluído**

- Autenticação, Página Inicial e Dashboard
- Clientes, Matrículas, Planos, Check-in e Presenças
- Avaliações Físicas, Fichas de Anamnese e Perguntas de Saúde
- Ficha de Treino, Exercícios, Grupos Musculares, Grupos e Turmas
- Contas a Receber, Contas a Pagar, Caixas, Despesas Fixas e Relatórios
- Prospecção, Contratos, Pagamentos, Colaboradores, Fornecedores, Pontuação, Produtos e Enquetes
- Inteligência e Automação, Configurações, Modelo Ficha e Aplicativo

**Fora do escopo**

- Integrações reais com Pagar.me e outros sistemas externos
- Alteração ou exclusão de dados reais da academia
- Dispositivos móveis e aplicativo nativo
- Testes de performance, carga e segurança aprofundada
- Testes de permissão entre perfis distintos

## Metodologia

Os casos de teste foram escritos no formato BDD (Gherkin), com a estrutura Dado, Quando e Então, e organizados em um arquivo por requisito funcional. A execução combinou as seguintes técnicas:

- Caminho feliz
- Testes negativos
- Particionamento de equivalência
- Análise de valor limite
- Testes exploratórios

Todos os registros criados durante os testes utilizam o prefixo `QA_`, de modo a não interferir nos dados reais da academia. A execução dos casos é registrada em vídeo, gravado com a ferramenta JAM ou armazenado na pasta de vídeos do projeto, exceto quando a gravação exporia credenciais do sistema.

## Documentação

| Documento | Conteúdo |
| --- | --- |
| [Análise de Requisitos](Sifit/1-Analise%20de%20requisitos.md) | Requisitos funcionais RF01 a RF31, um por tela ou submódulo |
| [Plano de Testes](Sifit/2-plano%20de%20testes.md) | Escopo, técnicas, ferramentas, cronograma e critérios de aceitação |
| [Relatório de Bugs](Sifit/3-Relatorio-de-Bugs.md) | Falhas encontradas, com passos de reprodução e evidências |
| [Relatório de Execução](Sifit/4-%20Relatorio%20dos%20testes.md) | Resumo da execução, cobertura por módulo e conclusão |
| [Cenários de Teste](Sifit/Cenarios%20de%20testes) | Casos de teste em BDD, um arquivo por requisito funcional |
| [Vídeos](Sifit/Videos) | Gravações de evidência da execução dos testes |
