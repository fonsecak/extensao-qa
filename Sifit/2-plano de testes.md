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
* Clientes.
* Matrículas e Planos.
* Check-in e Presenças.
* Avaliações e Saúde: Fichas Anamnese, Modelos, Categorias e Perguntas.
* Treinamento: Ficha de Treino, Exercícios, Grupos Musculares e Objetivos Treino.
* Grupos e Turmas.
* Consultas de Contas a Receber, Contas a Pagar, Caixas e Despesas Fixas.
* Relatórios.
* Comercial: Prospecção, Modelos Contrato, Tipos de Pagamento e Bandeiras.
* Gestão: Colaboradores, Funções, Fornecedores, Tipos de Documentos, Atividades, Pontuação, Produtos e Enquetes.
* Consulta dos recursos de Inteligência & Automação e Resultados IA.
* Consulta de Configurações, Modelo Ficha e Aplicativo.

**Excluído:**

* Testes de integração com Pagar.me e outros sistemas externos.
* Cobranças, pagamentos e outras movimentações financeiras reais.
* Exclusão ou alteração de dados reais de clientes.
* Disparos de automações e alterações globais nas configurações.
* Testes em dispositivos móveis ou no aplicativo nativo.
* Testes de performance, carga e segurança.
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
| RF04 | Matrículas e Planos | Alta |
| RF05 | Check-in e Presenças | Alta |
| RF06 | Avaliações e Saúde | Média |
| RF07 | Treinamento | Média |
| RF08 | Grupos e Turmas | Média |
| RF09 | Contas a Receber, Contas a Pagar, Caixas e Despesas Fixas | Alta |
| RF10 | Relatórios | Média |
| RF11 | Comercial | Baixa |
| RF12 | Gestão | Baixa |
| RF13 | Inteligência | Baixa |
| RF14 | Configurações | Baixa |

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
