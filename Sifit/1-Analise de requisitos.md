## **Requisitos Funcionais Detalhados para Testes Manuais**

**Sistema:** Sifit — https://sifit.centrion.com.br

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

**Descrição**: O sistema deve permitir a consulta, o cadastro e a edição de clientes, conforme as permissões do usuário.

* **Funcionalidades esperadas**:

 * Consulta dos clientes cadastrados.
 * Cadastro de um novo cliente.
 * Edição dos dados de um cliente existente.
 * Validação dos campos obrigatórios.
 * Validação de cadastros duplicados, conforme as regras da academia.

---

### **RF04 - Matrículas e Planos**

**Descrição**: O sistema deve permitir o vínculo entre o cliente e o plano contratado.

* **Funcionalidades esperadas**:

 * Consulta de matrículas e planos.
 * Vínculo da matrícula com o cliente e o plano correspondentes.
 * Exibição dos valores, da vigência e da situação da matrícula, conforme as regras da academia.

---

### **RF05 - Check-in e Presenças**

**Descrição**: O sistema deve permitir o registro e a consulta das presenças dos clientes.

* **Funcionalidades esperadas**:

 * Registro de check-in para o cliente correspondente.
 * Consulta das presenças registradas.
 * Validação das condições para realizar o check-in, conforme as regras da academia.
 * Tratamento de check-ins repetidos, conforme as regras da academia.

---

### **RF06 - Avaliações e Saúde**

**Descrição**: O sistema deve permitir a consulta e o registro de avaliações e fichas de anamnese vinculadas ao cliente.

* **Funcionalidades esperadas**:

 * Consulta e registro de avaliações.
 * Consulta e registro de Fichas Anamnese.
 * Vínculo das avaliações e das fichas com o cliente correspondente.
 * Acesso aos menus Modelos, Categorias e Perguntas da área de Saúde.
 * Acesso às informações conforme as permissões do usuário.

---

### **RF07 - Treinamento**

**Descrição**: O sistema deve permitir a consulta e a organização das fichas de treino e dos exercícios.

* **Funcionalidades esperadas**:

 * Consulta e organização da Ficha de Treino.
 * Consulta dos Exercícios.
 * Consulta dos Grupos Musculares e dos Objetivos Treino.
 * Vínculo entre fichas, exercícios, grupos musculares e objetivos, conforme o funcionamento das telas.

---

### **RF08 - Grupos e Turmas**

**Descrição**: O sistema deve permitir a consulta e a manutenção dos grupos e das turmas da academia.

* **Funcionalidades esperadas**:

 * Consulta dos grupos e das turmas cadastrados.
 * Manutenção dos grupos e das turmas, conforme as permissões do usuário.
 * Validação de participantes, horários e capacidade, quando essas regras se aplicarem.

---

### **RF09 - Contas a Receber, Contas a Pagar, Caixas e Despesas Fixas**

**Descrição**: O sistema deve permitir a consulta das informações financeiras da academia.

* **Funcionalidades esperadas**:

 * Consulta de Contas a Receber e Contas a Pagar.
 * Consulta de Caixas e Despesas Fixas.
 * Aplicação dos filtros disponíveis nas telas.
 * Exibição dos valores, das datas e das situações de acordo com os registros cadastrados.

---

### **RF10 - Relatórios**

**Descrição**: O sistema deve permitir a consulta de relatórios com base nos dados cadastrados.

* **Funcionalidades esperadas**:

 * Acesso aos relatórios disponíveis.
 * Aplicação dos filtros do relatório.
 * Exibição dos resultados de acordo com os filtros utilizados e os registros de origem.
 * Exportação dos resultados, caso essa opção esteja disponível.

---

### **RF11 - Comercial**

**Descrição**: O sistema deve permitir a consulta e os cadastros da área comercial, conforme as regras de cada menu.

* **Funcionalidades esperadas**:

 * Acesso ao menu Prospecção.
 * Consulta dos Modelos Contrato, Tipos de Pagamento e Bandeiras.
 * Cadastro de informações nos menus que disponibilizarem essa opção.
 * Validação dos dados conforme as regras de cada cadastro.

Os Planos estão relacionados ao RF04. O menu Pagar.me faz parte do levantamento, mas os testes da integração e das operações reais ficam fora da primeira etapa.

---

### **RF12 - Gestão**

**Descrição**: O sistema deve permitir a consulta e os cadastros da área de gestão, conforme as permissões do usuário.

* **Funcionalidades esperadas**:

 * Acesso aos menus Colaboradores, Funções e Fornecedores.
 * Acesso aos menus Tipos de Documentos, Atividades e Pontuação.
 * Acesso aos menus Produtos e Enquetes.
 * Consulta e cadastro de informações conforme as opções disponíveis em cada menu.
 * Validação dos dados conforme as regras de cada cadastro.

---

### **RF13 - Inteligência**

**Descrição**: O sistema deve permitir o acesso aos recursos de Inteligência & Automação e Resultados IA.

* **Funcionalidades esperadas**:

 * Acesso ao menu Inteligência & Automação.
 * Consulta dos retornos e do histórico disponíveis em Resultados IA.
 * Verificação das entradas e dos resultados conforme o funcionamento das telas.

---

### **RF14 - Configurações**

**Descrição**: O sistema deve permitir a consulta das configurações disponíveis para o perfil administrativo.

* **Funcionalidades esperadas**:

 * Acesso ao menu Configurações.
 * Consulta das opções de Modelo Ficha.
 * Consulta das opções do menu Aplicativo.

Nesta etapa, os testes financeiros serão feitos por consulta, sem movimentações reais. Alterações nas configurações e execução de automações dependem da definição do ambiente e das operações permitidas.
