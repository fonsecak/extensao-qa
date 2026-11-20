# Sifit: Testes Funcionais Manuais

Projeto de garantia de qualidade desenvolvido na disciplina de Extensão em Qualidade de Software. O trabalho avalia o Sifit, sistema de gestão de academias, por meio de testes funcionais manuais que cobrem consulta, cadastro, edição e exclusão nos módulos de clientes, matrículas, planos, check-in, avaliações físicas, treinamento, financeiro, comercial, gestão e configurações.

O objetivo é verificar se as funcionalidades se comportam conforme os requisitos levantados, observando fluxos de uso, validações de campos, mensagens de erro e consistência dos dados exibidos, e registrar cada falha com evidências reproduzíveis.

## Sumário

- [Visão geral](#visão-geral)
- [Resultados](#resultados)
- [Cobertura por área](#cobertura-por-área)
- [Escopo](#escopo)
- [Metodologia](#metodologia)
- [Evidências](#evidências)
- [Estrutura do repositório](#estrutura-do-repositório)
- [Documentação](#documentação)

## Visão geral

| Item | Descrição |
| --- | --- |
| Sistema avaliado | Sifit, sistema de gestão de academias |
| Tipo de teste | Funcional manual |
| Ambiente | Alfa ([sifitalfa.centrion.com.br](https://sifitalfa.centrion.com.br)) |
| Período de execução | 13/10/2026 a 18/11/2026 |
| Plataforma | Windows 11 e Google Chrome |
| Perfil utilizado | Administrativo |
| Ferramentas | Google Chrome, DevTools, JAM e Markdown |

## Resultados

| Indicador | Total |
| --- | :---: |
| Requisitos funcionais mapeados | **31** |
| Casos de teste executados | **98** |
| Casos com falha | **16** |
| Bugs registrados | **16** |

### Bugs por severidade

| Severidade | Quantidade | Bugs |
| --- | :---: | --- |
| Alta | 4 | SIFIT-BUG-009, 011, 013 e 015 |
| Média | 9 | SIFIT-BUG-001, 003, 004, 005, 006, 007, 010, 014 e 016 |
| Baixa | 3 | SIFIT-BUG-002, 008 e 012 |

Todos os bugs estão com status **Aberto**.

### Principal achado

Quatro fluxos centrais de cadastro falham com erro do servidor (HTTP 400 e 500). Trata-se de um padrão sistêmico, e não de falhas isoladas, com impacto direto nas operações mais frequentes da academia.

| Bug | Fluxo afetado | Sintoma |
| --- | --- | --- |
| SIFIT-BUG-009 | Cadastro de matrícula | "Erro ao Cadastrar com Assinatura" |
| SIFIT-BUG-011 | Avaliação física | Erro interno ao salvar a avaliação preenchida |
| SIFIT-BUG-013 | Cadastro de plano | "Erro ao salvar plano" |
| SIFIT-BUG-015 | Ficha de treino | "Erro ao salvar Ficha" |

Recomenda-se que esses quatro defeitos sejam tratados com prioridade máxima antes da liberação do sistema para uso real.

As demais falhas se concentram em quatro grupos:

- Validação insuficiente de dados, como produto ativo sem nome e período de relatório invertido.
- Divergência entre o dado cadastrado e o dado exibido, como enquetes, anamneses e check-ins.
- Mensagens de erro que não refletem o resultado real da operação.
- Exibição de credenciais sem mascaramento na tela de Configurações.

## Cobertura por área

| Área | Requisitos | Bugs |
| --- | --- | :---: |
| Acesso | RF01 Login, RF02 Página Inicial e Dashboard | 0 |
| Operação da academia | RF03 Clientes, RF04 Matrículas, RF05 Planos, RF06 Check-in e Presenças | 6 |
| Saúde e avaliação | RF07 Avaliações Físicas, RF08 Fichas Anamnese, RF09 Modelos, Categorias e Perguntas de Saúde | 2 |
| Treinamento | RF10 Ficha de Treino, RF11 Exercícios, RF12 Grupos Musculares e Objetivos, RF13 Grupos, RF14 Turmas | 1 |
| Financeiro | RF15 Contas a Receber, RF16 Contas a Pagar, RF17 Caixas, RF18 Despesas Fixas, RF19 Relatórios | 1 |
| Comercial | RF20 Prospecção, RF21 Modelos de Contrato, RF22 Tipos de Pagamento e Bandeiras | 1 |
| Gestão | RF23 Colaboradores e Funções, RF24 Fornecedores e Tipos de Documentos, RF25 Pontuação, RF26 Produtos, RF27 Enquetes, RF28 Inteligência e Automação | 3 |
| Configurações | RF29 Configurações, RF30 Modelo Ficha, RF31 Aplicativo | 2 |

O detalhamento por requisito, incluindo quais módulos tiveram ações de escrita testadas, está no [Relatório de Execução](Sifit/4-%20Relatorio%20dos%20testes.md).

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
- Testes de permissão entre perfis distintos, já que apenas a conta administrativa estava disponível

Ações que afetariam a operação real da academia, como executar automações, alterar configurações ou enviar notificações a alunos pelo aplicativo, foram verificadas apenas em modo de consulta.

## Metodologia

### Técnicas aplicadas

- Caminho feliz
- Testes negativos
- Particionamento de equivalência
- Análise de valor limite
- Testes exploratórios

### Escrita dos casos de teste

Os casos de teste seguem o formato BDD (Gherkin) e estão organizados em um arquivo por requisito funcional. Cada caso possui identificador, descrição, pré-condições, passos, critérios de aceitação, resultado obtido e evidência. Exemplo do caso C25-CT01:

```gherkin
DADO que estamos autenticados no Sifit
QUANDO clicarmos no menu "Pontuação"
ENTÃO a tela deve ser exibida com os indicadores "Total", "Ativos", "Por período" e "Mensais"
QUANDO clicarmos na ação de visualizar de uma pontuação
ENTÃO devem ser exibidos o nome, o período, o tipo, o status e a seção "Produtos de resgate"
```

### Registro de bugs

Cada bug é registrado com identificador no padrão `SIFIT-BUG-000`, severidade, prioridade de correção, status, passo a passo para reprodução, comportamento esperado e obtido, ambiente, funcionalidade afetada, caso de teste relacionado e evidências.

### Dados de teste

Todos os registros criados durante a execução utilizam o prefixo `QA_`, de modo a não interferir nos dados reais da academia. Somente registros com esse prefixo podem ser editados ou excluídos durante os testes.

## Evidências

A execução dos casos de teste é registrada em vídeo, de duas formas:

- **Links do JAM**, inseridos diretamente no caso de teste.
- **Arquivos de vídeo**, armazenados na pasta [Sifit/Videos](Sifit/Videos) e referenciados no caso de teste correspondente.

A gravação não é realizada quando poderia expor credenciais ou dados sensíveis do sistema. Nesses casos, o motivo é descrito no próprio caso de teste.

## Estrutura do repositório

```text
extensao-qa
  README.md
  Sifit
    1-Analise de requisitos.md
    2-plano de testes.md
    3-Relatorio-de-Bugs.md
    4- Relatorio dos testes.md
    Cenarios de testes      Casos de teste, um arquivo por requisito (CT_RF01 a CT_RF31)
    Videos                  Gravações de evidência da execução
  OrangeHRM                 Modelo de referência da disciplina, aplicado ao OrangeHRM Demo
```

## Documentação

| Documento | Conteúdo |
| --- | --- |
| [Análise de Requisitos](Sifit/1-Analise%20de%20requisitos.md) | Requisitos funcionais RF01 a RF31, um por tela ou submódulo |
| [Plano de Testes](Sifit/2-plano%20de%20testes.md) | Identificação, objetivo, escopo, ferramentas, técnicas e critérios de aceitação e de saída |
| [Relatório de Bugs](Sifit/3-Relatorio-de-Bugs.md) | Falhas encontradas, com severidade, passos de reprodução e evidências |
| [Relatório de Execução](Sifit/4-%20Relatorio%20dos%20testes.md) | Resumo da execução, cobertura por módulo, conclusão e análise de causa raiz |
| [Cenários de Teste](Sifit/Cenarios%20de%20testes) | Casos de teste em BDD, um arquivo por requisito funcional |
| [Vídeos](Sifit/Videos) | Gravações de evidência da execução dos testes |
