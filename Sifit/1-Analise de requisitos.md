## **Requisitos Funcionais Detalhados para Testes Manuais**

**Sistema:** Sifit — https://sifitalfa.centrion.com.br

### **RF01 - Autenticação de Usuário**

* O sistema deve permitir que o usuário realize login com suas credenciais válidas.
* O sistema deve exibir uma mensagem de erro em caso de login inválido.
* O sistema deve encerrar a sessão quando o usuário sair.

---

### **RF02 - Página Inicial e Dashboard**

**Descrição**: Após o login, o sistema deve exibir a área inicial e permitir o acesso aos menus disponíveis para o usuário.

* **Funcionalidades esperadas**:

 * Exibição da Página Inicial e do Dashboard.
 * Navegação pelos menus do sistema.
 * Exibição dos indicadores de acordo com os filtros utilizados e os dados cadastrados.

---

### **RF03 - Clientes**

**Descrição**: O sistema deve permitir a consulta, o cadastro, a edição e a exclusão de clientes, conforme as permissões do usuário.

* **Funcionalidades esperadas**:

 * Consulta dos clientes cadastrados, com busca por nome.
 * Cadastro de um novo cliente, com os dados de identificação, documentos, contato, endereço e aplicativo.
 * Edição dos dados de um cliente existente.
 * Exclusão de um cliente, mediante confirmação.
 * Validação dos campos obrigatórios.

---

### **RF04 - Matrículas**

**Descrição**: O sistema deve permitir a consulta, o cadastro, a edição e o cancelamento das matrículas dos clientes.

* **Funcionalidades esperadas**:

 * Consulta de matrículas, com busca por código ou nome.
 * Cadastro de uma nova matrícula, vinculando o cliente, a modalidade, o tipo de pagamento e o dia de vencimento.
 * Edição dos dados de uma matrícula existente.
 * Cancelamento de uma matrícula, mediante confirmação e motivo informado.
 * Exibição dos valores, da vigência e da situação da matrícula, conforme as regras da academia.

---

### **RF05 - Planos**

**Descrição**: O sistema deve permitir a consulta e o cadastro dos planos oferecidos pela academia.

* **Funcionalidades esperadas**:

 * Consulta dos planos cadastrados, com busca por nome.
 * Cadastro de um novo plano, incluindo a opção de integração com o Pagar.me.
 * Validação dos campos obrigatórios.

---

### **RF06 - Check-in e Presenças**

**Descrição**: O sistema deve permitir o registro e a consulta das presenças dos clientes.

* **Funcionalidades esperadas**:

 * Registro de check-in para o cliente correspondente, pela listagem ou pela entrada rápida por código.
 * Consulta das presenças registradas, por período.
 * Atualização dos indicadores e do status de cada cliente após o registro de um check-in.

---

### **RF07 - Avaliações Físicas**

**Descrição**: O sistema deve permitir a consulta, o agendamento e o preenchimento das avaliações físicas dos clientes.

* **Funcionalidades esperadas**:

 * Consulta das avaliações agendadas e realizadas.
 * Cadastro (agendamento) de uma nova avaliação.
 * Preenchimento dos dados da avaliação (IMC, circunferência, teste físico, composição corporal).
 * Vínculo das avaliações com o cliente correspondente.

---

### **RF08 - Fichas Anamnese**

**Descrição**: O sistema deve permitir a consulta e o registro das fichas de anamnese vinculadas ao cliente.

* **Funcionalidades esperadas**:

 * Consulta das fichas de anamnese.
 * Aplicação de uma nova ficha de anamnese a um cliente.
 * Vínculo das fichas com o cliente correspondente.

---

### **RF09 - Modelos, Categorias e Perguntas de Saúde**

**Descrição**: O sistema deve permitir a consulta e o cadastro dos modelos de anamnese, das categorias e das perguntas utilizadas na área de Saúde.

* **Funcionalidades esperadas**:

 * Consulta e cadastro de Modelos de Anamnese.
 * Consulta e cadastro de Categorias de Saúde.
 * Consulta e cadastro de Perguntas.

---

### **RF10 - Ficha de Treino**

**Descrição**: O sistema deve permitir a consulta e a organização das fichas de treino dos alunos.

* **Funcionalidades esperadas**:

 * Consulta das fichas de treino cadastradas.
 * Abertura do formulário de cadastro de uma ficha de treino, com vínculo ao aluno, ao personal, ao objetivo e ao período.

---

### **RF11 - Exercícios**

**Descrição**: O sistema deve permitir a consulta e o cadastro dos exercícios disponíveis para compor as fichas de treino.

* **Funcionalidades esperadas**:

 * Consulta da biblioteca de exercícios.
 * Cadastro de um novo exercício, com vínculo ao grupo muscular correspondente.

---

### **RF12 - Grupos Musculares e Objetivos de Treino**

**Descrição**: O sistema deve permitir a consulta e o cadastro dos grupos musculares e dos objetivos de treino utilizados na organização dos exercícios e das fichas.

* **Funcionalidades esperadas**:

 * Consulta e cadastro de Grupos Musculares.
 * Consulta e cadastro de Objetivos de Treino.

---

### **RF13 - Grupos**

**Descrição**: O sistema deve permitir a consulta e a manutenção dos grupos de atividades da academia.

* **Funcionalidades esperadas**:

 * Consulta dos grupos cadastrados, com os filtros disponíveis.
 * Manutenção dos grupos, conforme as permissões do usuário.

---

### **RF14 - Turmas**

**Descrição**: O sistema deve permitir a consulta e a manutenção das turmas da academia.

* **Funcionalidades esperadas**:

 * Consulta das turmas cadastradas, com os filtros disponíveis.
 * Visualização das informações detalhadas de uma turma (participantes, horários, capacidade).

---

### **RF15 - Contas a Receber**

**Descrição**: O sistema deve permitir a consulta das contas a receber da academia.

* **Funcionalidades esperadas**:

 * Consulta dos recebimentos cadastrados, por status e forma de pagamento.
 * Aplicação dos filtros disponíveis na tela.

---

### **RF16 - Contas a Pagar**

**Descrição**: O sistema deve permitir a consulta das contas a pagar da academia.

* **Funcionalidades esperadas**:

 * Consulta das despesas e dos pagamentos cadastrados.
 * Aplicação dos filtros disponíveis na tela.

---

### **RF17 - Caixas**

**Descrição**: O sistema deve permitir a consulta do movimento de caixa da academia.

* **Funcionalidades esperadas**:

 * Consulta do movimento de caixa, normal ou detalhado.
 * Aplicação dos filtros disponíveis na tela.

---

### **RF18 - Despesas Fixas**

**Descrição**: O sistema deve permitir a consulta das despesas fixas cadastradas pela academia.

* **Funcionalidades esperadas**:

 * Consulta das despesas fixas, com seus valores, datas e situações.

---

### **RF19 - Relatórios**

**Descrição**: O sistema deve permitir a geração de relatórios com base nos dados cadastrados.

* **Funcionalidades esperadas**:

 * Acesso aos modelos de relatório disponíveis.
 * Aplicação dos filtros de período e dos filtros específicos de cada modelo.
 * Geração do relatório em formato PDF.
 * Validação do período informado antes da geração.

---

### **RF20 - Prospecção**

**Descrição**: O sistema deve permitir a consulta e o cadastro de leads no funil comercial da academia.

* **Funcionalidades esperadas**:

 * Consulta dos leads cadastrados, com busca e filtro por estágio.
 * Cadastro de um novo lead, com os dados de contato e o estágio inicial.

---

### **RF21 - Modelos de Contrato**

**Descrição**: O sistema deve permitir a consulta e o cadastro dos modelos de contrato utilizados nas matrículas.

* **Funcionalidades esperadas**:

 * Consulta dos modelos de contrato cadastrados.
 * Cadastro de um novo modelo, com o uso de variáveis dinâmicas e a pré-visualização do texto.

---

### **RF22 - Tipos de Pagamento e Bandeiras**

**Descrição**: O sistema deve permitir a consulta e o cadastro dos tipos de pagamento e das bandeiras de cartão aceitos pela academia.

* **Funcionalidades esperadas**:

 * Consulta dos Tipos de Pagamento, com busca por nome.
 * Consulta e cadastro de Bandeiras de Cartão, com taxas e parcelas.

O menu Pagar.me faz parte do levantamento, mas os testes da integração e das operações reais ficam fora da primeira etapa.

---

### **RF23 - Colaboradores e Funções**

**Descrição**: O sistema deve permitir a consulta dos colaboradores e das funções da academia.

* **Funcionalidades esperadas**:

 * Consulta dos colaboradores cadastrados, com busca por nome.
 * Consulta das funções cadastradas, com os indicadores de Personal e Avaliador.

---

### **RF24 - Fornecedores e Tipos de Documentos**

**Descrição**: O sistema deve permitir a consulta dos fornecedores e dos tipos de documentos utilizados nos cadastros financeiros e de colaboradores.

* **Funcionalidades esperadas**:

 * Consulta dos fornecedores cadastrados.
 * Consulta dos tipos de documentos, com a aplicação correspondente (Colaborador ou Conta/Fornecedor).

---

### **RF25 - Pontuação**

**Descrição**: O sistema deve permitir a consulta e o cadastro dos desafios de pontuação da academia.

* **Funcionalidades esperadas**:

 * Consulta dos desafios de pontuação cadastrados.
 * Visualização dos detalhes de um desafio e dos produtos de resgate vinculados.

---

### **RF26 - Produtos**

**Descrição**: O sistema deve permitir a consulta e o cadastro dos produtos da academia.

* **Funcionalidades esperadas**:

 * Consulta dos produtos cadastrados, com nome, tipo, valor e status.
 * Validação dos campos obrigatórios no cadastro.

---

### **RF27 - Enquetes**

**Descrição**: O sistema deve permitir a consulta e o cadastro das enquetes disponibilizadas aos alunos.

* **Funcionalidades esperadas**:

 * Consulta das enquetes cadastradas, com a pergunta correspondente.
 * Cadastro de uma nova enquete.

---

### **RF28 - Inteligência e Automação**

**Descrição**: O sistema deve permitir o acesso aos recursos de automação e aos resultados gerados pela Inteligência Sifit.

* **Funcionalidades esperadas**:

 * Consulta das automações ativas e disponíveis.
 * Abertura da configuração de uma automação.
 * Consulta dos resultados da Inteligência, com filtro por período.

---

### **RF29 - Configurações**

**Descrição**: O sistema deve permitir a consulta e a alteração das configurações gerais da academia.

* **Funcionalidades esperadas**:

 * Acesso às abas Home, Biometria, Avaliação, Aniversário, Pagamento, Integrações e Design.
 * Consulta e alteração dos parâmetros de cada aba.

Nesta etapa, os testes financeiros serão feitos por consulta, sem movimentações reais. Alterações nas configurações e execução de automações dependem da definição do ambiente e das operações permitidas.

---

### **RF30 - Modelo Ficha**

**Descrição**: O sistema deve permitir a consulta dos modelos de ficha cadastrados.

* **Funcionalidades esperadas**:

 * Consulta dos modelos de ficha cadastrados, com título, criador e tipo.

---

### **RF31 - Aplicativo**

**Descrição**: O sistema deve permitir a consulta e a gestão do conteúdo exibido no aplicativo para os alunos.

* **Funcionalidades esperadas**:

 * Consulta dos indicadores de uso do aplicativo.
 * Consulta e cadastro de notificações.
 * Consulta das postagens e das denúncias.
