# Relatório Final de Execução de Testes - Sifit

**Sistema testado:** Sifit - Sistema de Gestão de Academia
**Responsável:** Gabriel Fonseca Proenca
**Data de execução:** 13/10/2026 a 18/11/2026
**Ambiente:** Alfa (https://sifitalfa.centrion.com.br)

* Sistema operacional: Windows 11
* Navegador: Google Chrome
* Perfil utilizado: Administrativo

---

## Resumo da Execução

| Total de Casos de Teste | Casos Falharam | Bugs Registrados |
| ----------------------- | --------------- | ------------------ |
| 98 | 16 | 16 |

---

## Cobertura por Módulo

| Código RF | Módulo | Escrita testada | Bugs encontrados | Bug(s) Associado(s) |
| --------- | ---------------------------------------- | :---: | ------------------ | -------------------- |
| RF01 | Login | Não | 0 | - |
| RF02 | Página Inicial e Dashboard | Não | 0 | - |
| RF03 | Clientes | Sim | 1 | SIFIT-BUG-008 |
| RF04 | Matrículas | Sim | 2 | SIFIT-BUG-001, SIFIT-BUG-009 |
| RF05 | Planos | Sim | 2 | SIFIT-BUG-012, SIFIT-BUG-013 |
| RF06 | Check-in e Presenças | Sim | 1 | SIFIT-BUG-010 |
| RF07 | Avaliações Físicas | Sim | 1 | SIFIT-BUG-011 |
| RF08 | Fichas Anamnese | Sim | 1 | SIFIT-BUG-014 |
| RF09 | Modelos, Categorias e Perguntas de Saúde | Não | 0 | - |
| RF10 | Ficha de Treino | Sim | 1 | SIFIT-BUG-015 |
| RF11 | Exercícios | Sim | 0 | - |
| RF12 | Grupos Musculares e Objetivos de Treino | Sim | 0 | - |
| RF13 | Grupos | Sim | 0 | - |
| RF14 | Turmas | Sim | 0 | - |
| RF15 | Contas a Receber | Não (só consulta) | 0 | - |
| RF16 | Contas a Pagar | Não (só consulta) | 0 | - |
| RF17 | Caixas | Não (só consulta) | 0 | - |
| RF18 | Despesas Fixas | Não (só consulta) | 0 | - |
| RF19 | Relatórios | Sim | 1 | SIFIT-BUG-002 |
| RF20 | Prospecção | Sim | 1 | SIFIT-BUG-003 |
| RF21 | Modelos de Contrato | Parcial (edição) | 0 | - |
| RF22 | Tipos de Pagamento e Bandeiras | Parcial (cadastro) | 0 | - |
| RF23 | Colaboradores e Funções | Não | 0 | - |
| RF24 | Fornecedores e Tipos de Documentos | Não | 0 | - |
| RF25 | Pontuação | Não | 0 | - |
| RF26 | Produtos | Sim | 1 | SIFIT-BUG-004 |
| RF27 | Enquetes | Sim | 2 | SIFIT-BUG-005, SIFIT-BUG-016 |
| RF28 | Inteligência e Automação | Não (afeta operação real) | 0 | - |
| RF29 | Configurações | Não (afeta operação real) | 2 | SIFIT-BUG-006 |
| RF30 | Modelo Ficha | Não | 1 | SIFIT-BUG-007 |
| RF31 | Aplicativo | Não (notificação real a alunos) | 0 | - |

---

## Resumo dos Bugs Reportados

| ID | Título | Severidade | Status |
| -------------- | ------------------------------------------------------------------------------ | ---------- | ------ |
| SIFIT-BUG-001 | Erro interno ao buscar matrícula pelo código | A avaliar | Aberto |
| SIFIT-BUG-002 | Geração de relatório aceita período com data inicial posterior à data final | A avaliar | Aberto |
| SIFIT-BUG-003 | Busca de lead por nome não retorna resultados na Prospecção | A avaliar | Aberto |
| SIFIT-BUG-004 | Cadastro de produto sem nome permanece ativo e disponível para venda | A avaliar | Aberto |
| SIFIT-BUG-005 | Pergunta de enquete não é persistida no cadastro (listagem reflete isso) | A avaliar | Aberto |
| SIFIT-BUG-006 | Campos de credenciais exibidos sem máscara em Configurações | A avaliar | Aberto |
| SIFIT-BUG-007 | Modelo Ficha sem título e ação de alterar direciona para fluxo incorreto | A avaliar | Aberto |
| SIFIT-BUG-008 | Campo "Tipo Sanguíneo" exibe o literal "null" quando vazio | A avaliar | Aberto |
| SIFIT-BUG-009 | Não é possível cadastrar nova matrícula ("Erro ao Cadastrar com Assinatura") | Alta | Aberto |
| SIFIT-BUG-010 | Tela de Check-ins não reflete corretamente os registros de entrada | A avaliar | Aberto |
| SIFIT-BUG-011 | Erro interno ao salvar avaliação física preenchida | Alta | Aberto |
| SIFIT-BUG-012 | Campos "Código" e "Nome" sem rótulo associado no formulário de Plano | A avaliar | Aberto |
| SIFIT-BUG-013 | Não é possível cadastrar novo plano ("Erro ao salvar plano") | Alta | Aberto |
| SIFIT-BUG-014 | Anamnese aplicada com sucesso não aparece na listagem | A avaliar | Aberto |
| SIFIT-BUG-015 | Não é possível cadastrar nova ficha de treino ("Erro ao salvar Ficha") | Alta | Aberto |
| SIFIT-BUG-016 | Mensagem "Erro ao salvar enquete" exibida mesmo com sucesso do backend | A avaliar | Aberto |

---

## Achado consolidado: cadastros novos falhando no backend

O achado mais significativo desta rodada é um **padrão sistêmico**, não bugs isolados: o cadastro de **novos registros** (ação "criar", diferente de editar um já existente) falha com erro do servidor (HTTP 400/500) em múltiplos módulos distintos:

* Matrículas (SIFIT-BUG-009, HTTP 400)
* Planos (SIFIT-BUG-013, HTTP 500)
* Avaliações Físicas (SIFIT-BUG-011, HTTP 500)
* Fichas de Treino (SIFIT-BUG-015, HTTP 500)

Em contraste, cadastros em Clientes, Exercícios, Grupos Musculares, Objetivos de Treino, Grupos (Comercial), Turmas e Produtos funcionaram normalmente. Isso sugere que o problema está concentrado em fluxos que envolvem vínculos mais complexos (cliente + plano + pagamento, ou cliente + dados físicos), possivelmente relacionados a uma mudança recente de backend ou a uma dependência externa com falha (ex.: validação de assinatura/gateway). Recomenda-se investigação prioritária, dado o impacto direto na operação da academia.

Um segundo padrão identificado é **mensagens de erro que não refletem o resultado real**: o cadastro de Enquete (SIFIT-BUG-016) exibe "Erro ao salvar enquete" mesmo com o backend retornando sucesso (HTTP 200) e o registro sendo de fato criado — mas sem persistir corretamente o campo "Pergunta" (SIFIT-BUG-005). Isso indica possível inconsistência entre o que a API retorna e o que o frontend interpreta como sucesso, e merece atenção porque pode levar o usuário a tentar cadastrar o mesmo registro várias vezes.

---

## Observações sobre o Escopo Executado

* Os testes foram realizados no ambiente alfa (https://sifitalfa.centrion.com.br), com uma conta administrativa já autenticada.
* A estrutura de requisitos e de casos de teste foi reorganizada nesta rodada: os módulos antes agrupados (ex.: "Matrículas e Planos", "Avaliações e Saúde", "Treinamento", "Consultas Financeiras", "Comercial", "Gestão", "Configurações") foram desmembrados em requisitos funcionais específicos por tela, elevando a cobertura de 14 para 31 RFs. Essa reorganização é exclusivamente de documentação; nenhum teste anteriormente executado foi descartado.
* O escopo de execução foi ampliado para incluir ações de escrita (criar, editar, cancelar e excluir) em treze dos trinta e um módulos, usando exclusivamente registros de teste identificados pelo prefixo "QA_". Essa ampliação revelou a maior parte dos bugs críticos listados acima.
* Três categorias de ação foram deliberadamente não testadas, por risco de efeito colateral real: movimentações financeiras (Contas a Receber/Pagar, Caixas), alterações de configurações globais da academia, execução de automações reais (WhatsApp) e envio de notificações reais a alunos pelo Aplicativo.
* Evidências em vídeo (JAM) ficaram pendentes de gravação para a maior parte dos cenários desta e da rodada anterior.

---

## Conclusão

A execução dos testes manuais no Sifit cobriu os 31 requisitos funcionais mapeados, incluindo pela primeira vez ações de escrita em treze módulos. O achado mais relevante é o padrão sistêmico de falha em fluxos de cadastro novo (matrícula, plano, avaliação física, ficha de treino), todos retornando erro HTTP 400/500 do backend — um risco direto à operação diária da academia, já que esses são os fluxos mais usados no dia a dia (matricular aluno, aplicar avaliação). As demais falhas se dividem em: validação insuficiente de dados, inconsistência entre o dado cadastrado e o dado exibido, mensagens de erro que não refletem o resultado real, e exposição de credenciais em texto plano nas telas de Configurações.

Das 16 falhas registradas, quatro foram classificadas como Alta severidade (SIFIT-BUG-009, 011, 013, 015), todas bloqueando fluxos de cadastro principais. Recomenda-se que essas quatro sejam tratadas com prioridade máxima antes de qualquer liberação do ambiente para uso real pela academia.

### Identificação da Causa Raiz (Root Cause Analysis)

A identificação da causa raiz é uma etapa essencial no processo de garantia de qualidade (QA), pois busca entender por que um defeito ocorreu, indo além dos sintomas visíveis do problema. Essa análise ajuda a evitar recorrência de falhas, melhorando a qualidade do software a longo prazo.

Nesta execução, essa prática foi decisiva em pelo menos três momentos. Primeiro, ao investigar o bug de Enquetes (SIFIT-BUG-005), a hipótese inicial era de uma falha na listagem; o teste de cadastro de uma nova enquete revelou que a causa real está no próprio cadastro, que não persiste o campo "Pergunta" — e que, além disso, o frontend relata erro mesmo quando o backend confirma sucesso (SIFIT-BUG-016), uma segunda causa raiz distinta descoberta na mesma investigação. Segundo, ao testar o cadastro de Plano, um erro inicial de preenchimento (campo "Nome" não associado corretamente ao rótulo, SIFIT-BUG-012) quase mascarou o problema real: mesmo corrigindo o campo, o cadastro falhava com erro 500 do servidor (SIFIT-BUG-013) — ou seja, dois bugs distintos e independentes no mesmo fluxo, que só foram isolados ao reproduzir o problema passo a passo. Terceiro, o padrão repetido de falha 400/500 em quatro módulos de cadastro diferentes (matrícula, plano, avaliação, ficha de treino) só foi identificado como sistêmico — e não quatro problemas isolados — por comparar as respostas de rede entre os módulos.

A causa raiz pode estar em erros de lógica no código, falhas de validação, má comunicação entre equipes, requisitos mal definidos ou até inconsistências no ambiente de teste. Identificar corretamente a causa raiz permite que os desenvolvedores corrijam o erro de forma precisa e que o time evite retrabalhos, contribuindo para entregas mais estáveis, eficientes e com menor custo.
