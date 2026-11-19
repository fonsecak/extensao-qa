## **Plano de Testes - Sifit**

### 1. **Identificação**

* **Nome do Projeto**: Sifit - Sistema de Gestão de Academia
* **Versão Avaliada**: A confirmar
* **Ambiente de Testes**: https://sifit.centrion.com.br — tipo de ambiente a confirmar
* **Tipo de Teste**: Teste Funcional Manual
* **Data do Documento**: 05/10/2026
* **Responsável**: Gabriel Fonseca Proenca
* **Disciplina**: Extensão — Qualidade de Software
* **Perfil disponível**: Administrativo

---

### 2. **Objetivo**

Verificar manualmente as funcionalidades do Sifit previstas na análise de requisitos, observando os fluxos de uso, as validações dos campos, as mensagens de erro e os dados apresentados pelo sistema. Registrar os resultados e as falhas encontradas com evidências.

---

### 3. **Escopo**

**Incluído:**

* Autenticação de usuário e encerramento da sessão.
* Página Inicial e Dashboard.
* Clientes: consulta, cadastro, edição e exclusão.
* Matrículas: consulta, cadastro, edição e cancelamento.
* Planos: consulta e cadastro.
* Check-in e Presenças.
* Avaliações Físicas: consulta, agendamento e preenchimento.
* Fichas Anamnese: consulta e aplicação.
* Modelos, Categorias e Perguntas de Saúde.
* Ficha de Treino, Exercícios, Grupos Musculares e Objetivos de Treino.
* Grupos e Turmas.
* Contas a Receber, Contas a Pagar, Caixas e Despesas Fixas.
* Relatórios.
* Prospecção, Modelos de Contrato, Tipos de Pagamento e Bandeiras.
* Colaboradores, Funções, Fornecedores, Tipos de Documentos, Pontuação, Produtos e Enquetes.
* Inteligência e Automação, incluindo abertura da configuração de uma automação.
* Configurações, Modelo Ficha e Aplicativo.

**Excluído:**

* Testes de integração real com Pagar.me e outros sistemas externos.
* Exclusão ou alteração de dados reais de clientes da academia; apenas registros de teste, identificados pelo prefixo "QA_", podem ser criados, editados ou excluídos.
* Testes em dispositivos móveis ou no aplicativo nativo.
* Testes de performance, carga e segurança aprofundada.
* Testes de permissões entre diferentes perfis, enquanto houver apenas a conta administrativa.

---

### 4. **Ferramentas Utilizadas**

* Navegador Google Chrome, previsto para a execução inicial.
* Ferramentas de inspeção do navegador (DevTools), quando necessário.
* Arquivos Markdown para os casos de teste e relatórios.
* JAM para gravação dos vídeos de evidência.
* Captura de tela para complementar as evidências.
* Git para acompanhar as alterações dos documentos.

---

### 5. **Técnicas de Teste**

* Particionamento de equivalência.
* Análise de valor limite.
* Caminho feliz (Happy Path).
* Testes negativos.
* Testes exploratórios.

---

### 6. **Critérios de Aceitação**

* Todos os casos de teste devem passar com sucesso, conforme o resultado esperado.
* Nenhuma falha crítica deve estar presente em funcionalidades principais.
* Mensagens de erro e validações devem ser consistentes.

---

### 7. **Critérios de Saída (Exit Criteria)**

* Todos os testes do escopo foram executados.
* Falhas foram registradas, analisadas e reexecutadas se necessário.
* Documentação de evidências de sucesso e falhas está completa.
---

### 8. **Cronograma Estimado**

| Atividade | Data Início | Data Fim |
| --------------------------- | ----------- | ---------- |
| Planejamento de Testes | A definir | A definir |
| Criação de Casos de Teste | A definir | A definir |
| Execução dos Testes Manuais | A definir | A definir |
| Registro de Bugs e Retestes | A definir | A definir |
| Encerramento e Evidências | A definir | A definir |

---

### 9. **Módulos a Serem Testados**

| Código RF | Módulo | Prioridade |
| --------- | ------------------------ | ---------- |
| RF01 | Autenticação de Usuário | Alta |
| RF02 | Página Inicial e Dashboard | Média |
| RF03 | Clientes | Alta |
| RF04 | Matrículas | Alta |
| RF05 | Planos | Alta |
| RF06 | Check-in e Presenças | Alta |
| RF07 | Avaliações Físicas | Média |
| RF08 | Fichas Anamnese | Média |
| RF09 | Modelos, Categorias e Perguntas de Saúde | Baixa |
| RF10 | Ficha de Treino | Média |
| RF11 | Exercícios | Baixa |
| RF12 | Grupos Musculares e Objetivos de Treino | Baixa |
| RF13 | Grupos | Média |
| RF14 | Turmas | Média |
| RF15 | Contas a Receber | Alta |
| RF16 | Contas a Pagar | Alta |
| RF17 | Caixas | Alta |
| RF18 | Despesas Fixas | Média |
| RF19 | Relatórios | Média |
| RF20 | Prospecção | Baixa |
| RF21 | Modelos de Contrato | Baixa |
| RF22 | Tipos de Pagamento e Bandeiras | Baixa |
| RF23 | Colaboradores e Funções | Baixa |
| RF24 | Fornecedores e Tipos de Documentos | Baixa |
| RF25 | Pontuação | Baixa |
| RF26 | Produtos | Baixa |
| RF27 | Enquetes | Baixa |
| RF28 | Inteligência e Automação | Baixa |
| RF29 | Configurações | Baixa |
| RF30 | Modelo Ficha | Baixa |
| RF31 | Aplicativo | Baixa |

---

### 10. **Gestão de Defeitos**

* Bugs serão documentados com:

 * Título
 * Descrição
 * Passos para reproduzir
 * Evidência (print ou vídeo)
 * Gravidade (Crítica, Alta, Média, Baixa)
* Ferramenta sugerida: Trello (para simulação)

---

### 11. **Riscos Identificados**

| Risco | Impacto | Mitigação |
| -------------------------------------- | ------- | -------------------------------- |
| Sistema fora do ar | Alto | Registrar o impedimento e tentar novamente depois |
| Ambiente em uso pela academia | Alto | Confirmar as operações permitidas e utilizar dados fictícios |
| Regras das telas ainda não confirmadas | Alto | Esclarecer as regras antes de criar os casos |
| Muitos módulos para o prazo disponível | Alto | Executar primeiro os módulos de prioridade alta e registrar a cobertura alcançada |
| Apenas perfil administrativo disponível | Médio | Documentar a limitação dos testes de permissões |
| Dados pessoais nas evidências | Alto | Ocultar as informações antes de anexar as evidências |

---

### 12. **Entregáveis**

* Plano de Testes (.md ou .pdf)
* Casos de Teste (.md ou planilha)
* Evidências de Execução (prints organizados por RF)
* Registro de Bugs (se houver)
* Registro de Melhoria (se houver)
* Relatório Final de Execução
