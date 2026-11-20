# Relatório de Bugs

**Software:** Sifit

**QA responsável:** Gabriel Fonseca Proenca

**Data do registro:** 13/10/2026

---

### **Bug 01: Erro interno ao buscar matrícula pelo código**

| **ID** | **Descrição** |
| :--- | :--- |
| SIFIT-BUG-001 | Ao buscar uma matrícula pelo código, informando o valor `3` como exemplo, o sistema apresenta um erro interno. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| :--- |
| 1. Acessar o menu "Matrículas". |
| 2. Informar `3` no campo "Código". |
| 3. Clicar em "Buscar". |
| 4. Observar o erro interno exibido pelo sistema. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :--- | :--- |
| O sistema deve apresentar a matrícula correspondente ao código informado ou indicar que nenhum resultado foi encontrado. | O sistema apresenta um erro interno durante a busca. |

| **Ambiente** |
| :--- |
| Endereço: https://sifit.centrion.com.br/ |
| Navegador, versão e tipo de ambiente: a registrar. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :--- | :--- |
| Matrículas — busca por código | C04-CT02: Busca de matrícula por código ou nome (RF04 - Matrículas) |

| **Evidência(s)** |
| :--- |
| Link do vídeo do JAM: a adicionar. |

---

### **Bug 02: Geração de relatório aceita período com data inicial posterior à data final**

| **ID** | **Descrição** |
| :--- | :--- |
| SIFIT-BUG-002 | Na tela de Relatórios, o sistema aceita e processa a geração de um relatório mesmo quando a "Data Início" informada é posterior à "Data Fim", sem apresentar mensagem de validação. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Baixa | Baixa | Aberto |

| **Passo a passo para simular o bug** |
| :--- |
| 1. Acessar o menu "Relatórios". |
| 2. Selecionar qualquer modelo de relatório. |
| 3. Informar uma data posterior no campo "Data Início" em relação ao campo "Data Fim" (por exemplo, "31/12/2026" e "18/11/2026"). |
| 4. Clicar em "Gerar Relatório". |
| 5. Observar que a solicitação é processada normalmente, sem alerta sobre o período inválido. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :--- | :--- |
| O sistema deve impedir a geração e apresentar uma mensagem informando que o período é inválido. | O sistema aceita o período invertido e envia a solicitação para processamento (requisição `POST /api/relatorio/1` com `data_inicial` posterior a `data_final`). |

| **Ambiente** |
| :--- |
| Endereço: https://sifitalfa.centrion.com.br/relatorios |
| Navegador, versão e tipo de ambiente: a registrar. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :--- | :--- |
| Relatórios — geração por período | C19-CT05: Tentativa de geração com período invertido (RF19 - Relatórios) |

| **Evidência(s)** |
| :--- |
| Link do vídeo do JAM: a adicionar. |

---

### **Bug 03: Busca de lead por nome não retorna resultados na Prospecção**

| **ID** | **Descrição** |
| :--- | :--- |
| SIFIT-BUG-003 | Na tela de Prospecção, o campo "Buscar lead" indica aceitar busca por "Nome, e-mail, telefone ou código", mas a busca por nome não retorna nenhum resultado, mesmo para leads existentes e visíveis na listagem. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| :--- |
| 1. Acessar o menu "Prospecção". |
| 2. Identificar o nome de um lead já listado na tela (por exemplo, "Tasia Maria"). |
| 3. Informar esse nome, completo ou parcial, no campo "Buscar lead". |
| 4. Observar que a lista retorna "Nenhum lead encontrado". |
| 5. Repetir a busca informando o código do mesmo lead e observar que o resultado é encontrado normalmente. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :--- | :--- |
| A busca por nome deve retornar os leads correspondentes, conforme indicado no próprio campo de busca. | A busca por nome não retorna nenhum resultado; apenas a busca por código funciona. |

| **Ambiente** |
| :--- |
| Endereço: https://sifitalfa.centrion.com.br/prospeccao |
| Navegador, versão e tipo de ambiente: a registrar. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :--- | :--- |
| Prospecção — busca de lead | C20-CT02: Busca de lead por nome (RF20 - Prospecção) |

| **Evidência(s)** |
| :--- |
| Link do vídeo do JAM: a adicionar. |

---

### **Bug 04: Cadastro de produto sem nome permanece ativo e disponível para venda**

| **ID** | **Descrição** |
| :--- | :--- |
| SIFIT-BUG-004 | Na tela de Produtos, o produto de código 8 está cadastrado sem nome preenchido, com status "Ativo" e disponível para venda, com valor definido. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| :--- |
| 1. Acessar o menu "Produtos". |
| 2. Observar a linha de código 8 na listagem. |
| 3. Verificar que o campo "Nome" está em branco, enquanto "Tipo", "Valor" e "Status" estão preenchidos. |
| 4. Abrir a visualização do produto e confirmar que o campo "Nome" está vazio no cadastro. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :--- | :--- |
| O sistema deve exigir o preenchimento do nome do produto antes de permitir o cadastro ou a ativação. | Existe um produto ativo, disponível para venda, sem nome cadastrado. |

| **Ambiente** |
| :--- |
| Endereço: https://sifitalfa.centrion.com.br/produtos |
| Navegador, versão e tipo de ambiente: a registrar. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :--- | :--- |
| Produtos — cadastro | C26-CT01: Acesso à tela de Produtos (RF26 - Produtos) |

| **Evidência(s)** |
| :--- |
| Link do vídeo do JAM: a adicionar. |

---

### **Bug 05: Listagem de Enquetes não exibe a pergunta cadastrada**

| **ID** | **Descrição** |
| :--- | :--- |
| SIFIT-BUG-005 | Na tela de Enquetes, todos os registros listados exibem "Sem pergunta cadastrada" na coluna "Pergunta", mesmo quando a pergunta está de fato preenchida no cadastro da enquete. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| :--- |
| 1. Acessar o menu "Enquetes". |
| 2. Observar que todas as 35 enquetes listadas exibem "Sem pergunta cadastrada". |
| 3. Abrir a visualização da enquete de código 28 ("Manual SIFIT Horário preferido"). |
| 4. Observar que o campo "Pergunta" do formulário está preenchido com "Qual horário você prefere treinar?". |
| 5. (Causa raiz) Criar uma nova enquete, preenchendo Nome, Pergunta e uma Resposta, e clicar em "Salvar". |
| 6. Observar que o sistema exibe "Erro ao salvar enquete" mesmo com `POST /api/enquete/salvar/1` retornando HTTP 200 (sucesso) — ver SIFIT-BUG-016. |
| 7. Buscar a enquete recém-criada na listagem: ela aparece normalmente (nome e código corretos), mas também com "Sem pergunta cadastrada". |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :--- | :--- |
| A coluna "Pergunta" da listagem deve exibir a pergunta cadastrada em cada enquete. | A listagem exibe "Sem pergunta cadastrada" para todos os registros, independentemente do conteúdo real cadastrado. O teste de cadastro de uma nova enquete (passo 5) reproduziu o mesmo sintoma: a pergunta não é persistida pelo backend durante o cadastro, apesar do nome e da resposta terem sido salvos. A causa raiz provável está no endpoint `POST /api/enquete/salvar/1`, que não grava o campo de pergunta — e não na listagem, como a hipótese original sugeria. |

| **Ambiente** |
| :--- |
| Endereço: https://sifitalfa.centrion.com.br/enquetes |
| Navegador, versão e tipo de ambiente: a registrar. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :--- | :--- |
| Enquetes — listagem | C27-CT01: Acesso à tela de Enquetes e consistência da pergunta cadastrada (RF27 - Enquetes) |

| **Evidência(s)** |
| :--- |
| Link do vídeo do JAM: a adicionar. |

---

### **Bug 06: Campos de credenciais exibidos sem máscara em Configurações**

| **ID** | **Descrição** |
| :--- | :--- |
| SIFIT-BUG-006 | Nas abas "Biometria" e "Pagamento" da tela de Configurações, os campos "Senha" (acesso ao aparelho biométrico) e "Token Pagar.me" são exibidos em texto plano, sem máscara. Para comparação, o campo "Access Token" da aba "Integrações" é corretamente mascarado. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| :--- |
| 1. Acessar o menu "Configurações". |
| 2. Abrir a aba "Biometria" e observar o campo "Senha". |
| 3. Abrir a aba "Pagamento" e observar o campo "Token Pagar.me". |
| 4. Comparar com o campo "Access Token" da aba "Integrações", que é exibido mascarado. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :--- | :--- |
| Campos de credenciais e tokens de acesso devem ser exibidos mascarados, com opção de revelar quando necessário. | Os campos "Senha" (Biometria) e "Token Pagar.me" (Pagamento) exibem o valor em texto plano. |

| **Ambiente** |
| :--- |
| Endereço: https://sifitalfa.centrion.com.br/configuracoes |
| Navegador, versão e tipo de ambiente: a registrar. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :--- | :--- |
| Configurações — Biometria e Pagamento | C29-CT02 e C29-CT03 (RF29 - Configurações) |

| **Evidência(s)** |
| :--- |
| Link do vídeo do JAM: a adicionar. |

---

### **Bug 07: Modelo Ficha sem título e ação de alterar direciona para fluxo incorreto**

| **ID** | **Descrição** |
| :--- | :--- |
| SIFIT-BUG-007 | Na tela "Modelos de Ficha" (menu Configurações > Modelo Ficha), todos os registros exibem "Sem título" na coluna "Título", e a ação "Alterar" direciona para a rota de edição de Ficha de Treino de um aluno específico, em vez de um editor de modelo de ficha reutilizável. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| :--- |
| 1. Acessar o menu "Modelo Ficha". |
| 2. Observar que todos os seis registros listados exibem "Sem título". |
| 3. Clicar na ação "Alterar" do registro de código 1. |
| 4. Observar que a navegação leva à rota "/ficha-treino/alterar/1", com o título "Treino de Manual SIFIT Aluno Exemplo". |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :--- | :--- |
| A listagem deve exibir o título cadastrado de cada modelo, e a ação "Alterar" deve abrir o editor do modelo de ficha correspondente. | A listagem exibe "Sem título" para todos os registros, e a ação "Alterar" abre a ficha de treino de um aluno específico, não um modelo. |

| **Ambiente** |
| :--- |
| Endereço: https://sifitalfa.centrion.com.br/fichas-treino-modelo |
| Navegador, versão e tipo de ambiente: a registrar. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :--- | :--- |
| Configurações — Modelo Ficha | C30-CT01: Acesso à tela de Modelo Ficha (RF30 - Modelo Ficha) |

| **Evidência(s)** |
| :--- |
| Link do vídeo do JAM: a adicionar. |

---

### **Bug 08: Campo "Tipo Sanguíneo" exibe o literal "null" quando vazio**

| **ID** | **Descrição** |
| :--- | :--- |
| SIFIT-BUG-008 | Na tela de edição de cliente, o campo "Tipo Sanguíneo" exibe o texto literal "null" quando o campo não foi preenchido no cadastro, em vez de aparecer vazio. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Baixa | Baixa | Aberto |

| **Passo a passo para simular o bug** |
| :--- |
| 1. Cadastrar um novo cliente sem preencher o campo "Tipo Sanguíneo". |
| 2. Abrir a edição desse cliente ("Alterar dados"). |
| 3. Observar o conteúdo do campo "Tipo Sanguíneo". |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :--- | :--- |
| O campo deve aparecer vazio, com o placeholder correspondente. | O campo exibe o texto literal "null". |

| **Ambiente** |
| :--- |
| Endereço: https://sifitalfa.centrion.com.br/alterar-cliente |
| Navegador, versão e tipo de ambiente: a registrar. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :--- | :--- |
| Clientes — edição | C03-CT05: Edição de cliente cadastrado (RF03 - Clientes) |

| **Evidência(s)** |
| :--- |
| Link do vídeo do JAM: a adicionar. |

---

### **Bug 09: Não é possível cadastrar nova matrícula ("Erro ao Cadastrar com Assinatura")**

| **ID** | **Descrição** |
| :--- | :--- |
| SIFIT-BUG-009 | O cadastro de nova matrícula falha em toda tentativa, com a mensagem "Erro ao Cadastrar com Assinatura" e resposta HTTP 400 do backend, independentemente do plano ou do tipo de pagamento selecionado. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Alta | Alta (bloqueia o fluxo principal de matrícula) | Aberto |

| **Passo a passo para simular o bug** |
| :--- |
| 1. Acessar o menu "Matrículas". |
| 2. Clicar em "Cadastrar Matrícula". |
| 3. Buscar e selecionar um cliente sem matrícula ativa. |
| 4. Selecionar qualquer Modalidade (testado com "Treino Livre" e "Teste Final"). |
| 5. Selecionar qualquer Tipo de Pagamento (testado com "Manual SIFIT Pix" e "Dinheiro") e preencher o Dia de Vencimento. |
| 6. Clicar em "Salvar". |
| 7. Observar a mensagem "Não foi possível concluir — Erro ao Cadastrar com Assinatura". |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :--- | :--- |
| A matrícula deve ser cadastrada com sucesso e vinculada ao cliente selecionado. | O cadastro falha sempre, com `POST /api/salvar/matricula/1` retornando HTTP 400. |

| **Ambiente** |
| :--- |
| Endereço: https://sifitalfa.centrion.com.br/adicionar-matricula |
| Navegador, versão e tipo de ambiente: a registrar. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :--- | :--- |
| Matrículas — cadastro | C04-CT04: Cadastro de nova matrícula (RF04 - Matrículas) |

| **Evidência(s)** |
| :--- |
| Link do vídeo do JAM: a adicionar. |

---

### **Bug 10: Tela de Check-ins não reflete corretamente os registros de entrada**

| **ID** | **Descrição** |
| :--- | :--- |
| SIFIT-BUG-010 | Na tela de Check-ins, após registrar a entrada de um cliente (seja pelo botão "Registrar entrada" na listagem, seja pelo campo "Entrada rápida"), o indicador "Check-ins hoje" e o status da linha do cliente não são atualizados corretamente, mesmo com o backend confirmando o registro (HTTP 201) e o "Total de check-ins" do perfil do cliente sendo incrementado. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| :--- |
| 1. Acessar o menu "Check-in", com um cliente listado como "Pendente". |
| 2. Clicar em "Registrar entrada" na linha desse cliente. |
| 3. Observar que a linha continua "Pendente" e o indicador "Check-ins hoje" não reflete corretamente o total, mesmo após recarregar a página. |
| 4. Repetir o check-in do mesmo cliente usando o campo "Entrada rápida" (informando o código). |
| 5. Observar que o indicador "Check-ins hoje" não é incrementado, apesar de `POST /api/checkin/entrada/1` retornar HTTP 201. |
| 6. Confirmar no perfil do cliente ("Visualizar Cliente") que o "Total de check-ins" foi de fato incrementado em ambas as tentativas. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :--- | :--- |
| A tela de Check-ins deve refletir fielmente os registros de entrada, tanto no status da linha quanto no indicador "Check-ins hoje". | O backend registra os check-ins corretamente, mas a tela de Check-ins não reflete esse estado, criando risco de duplicidade (a recepção pode tentar registrar novamente, achando que não funcionou). |

| **Ambiente** |
| :--- |
| Endereço: https://sifitalfa.centrion.com.br/checkin |
| Navegador, versão e tipo de ambiente: a registrar. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :--- | :--- |
| Check-in — registro de entrada | C06-CT05: Registro de entrada e atualização da tela de Check-ins (RF06 - Check-in e Presenças) |

| **Evidência(s)** |
| :--- |
| Link do vídeo do JAM: a adicionar. |

---

### **Bug 11: Erro interno ao salvar avaliação física preenchida**

| **ID** | **Descrição** |
| :--- | :--- |
| SIFIT-BUG-011 | Ao preencher os dados de uma avaliação física agendada (altura e peso na aba IMC) e clicar em "Salvar", o sistema apresenta a mensagem "Erro ao salvar avaliação", com o backend retornando HTTP 500. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Alta | Alta (bloqueia o fluxo principal de avaliação) | Aberto |

| **Passo a passo para simular o bug** |
| :--- |
| 1. Acessar o menu "Avaliações". |
| 2. Clicar em "Fazer Avaliação" em uma avaliação com status "Pendente". |
| 3. Na aba "IMC", informar Altura (ex.: 1,75) e Peso (ex.: 80). |
| 4. Observar que o IMC é calculado corretamente na pré-visualização do formulário (ex.: "26 - Sobrepeso"). |
| 5. Clicar em "Salvar". |
| 6. Observar a mensagem "Erro ao salvar avaliação". |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :--- | :--- |
| A avaliação deve ser salva com sucesso e passar para o status "Realizado". | O salvamento falha, com `POST /api/avaliacao/salvarFeita/1` retornando HTTP 500. |

| **Ambiente** |
| :--- |
| Endereço: https://sifitalfa.centrion.com.br/avaliacoes |
| Navegador, versão e tipo de ambiente: a registrar. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :--- | :--- |
| Avaliações — preenchimento | C07-CT03: Preenchimento de uma avaliação agendada (RF07 - Avaliações Físicas) |

| **Evidência(s)** |
| :--- |
| Link do vídeo do JAM: a adicionar. |

---

### **Bug 12: Campos "Código" e "Nome" do formulário de Plano sem rótulo associado corretamente**

| **ID** | **Descrição** |
| :--- | :--- |
| SIFIT-BUG-012 | No formulário "Novo Plano", os campos de texto sob os rótulos "Código" e "Nome" não possuem associação de acessibilidade (`label`/`for`/`aria-label`) correta, o que pode levar leitores de tela e ferramentas de automação a preencher o campo errado. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Baixa | Baixa | Aberto |

| **Passo a passo para simular o bug** |
| :--- |
| 1. Acessar o menu "Planos". |
| 2. Clicar em "Novo Plano". |
| 3. Usando uma ferramenta de inspeção de acessibilidade (árvore de acessibilidade do navegador), localizar o campo associado ao rótulo "Nome". |
| 4. Observar que a árvore de acessibilidade não associa nenhum rótulo (`label`) a esse campo, e que o primeiro campo de texto do formulário (correspondente visualmente a "Código") é o único alcançável de forma direta, confundindo a ordem de preenchimento. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :--- | :--- |
| Cada campo do formulário deve ter um rótulo associado corretamente, de forma que leitores de tela e ferramentas de preenchimento automático identifiquem o campo certo. | Os campos "Código" e "Nome" não têm rótulo associado, o que resulta em preenchimento no campo errado ao usar ferramentas de acessibilidade. |

| **Ambiente** |
| :--- |
| Endereço: https://sifitalfa.centrion.com.br/planos |
| Navegador, versão e tipo de ambiente: a registrar. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :--- | :--- |
| Planos — cadastro | C05-CT04: Associação incorreta dos campos "Código" e "Nome" no formulário (RF05 - Planos) |

| **Evidência(s)** |
| :--- |
| Link do vídeo do JAM: a adicionar. |

---

### **Bug 13: Não é possível cadastrar novo plano ("Erro ao salvar plano")**

| **ID** | **Descrição** |
| :--- | :--- |
| SIFIT-BUG-013 | O cadastro de novo plano falha com a mensagem "Erro ao salvar plano", com o backend retornando HTTP 500, mesmo com todos os campos obrigatórios preenchidos corretamente. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Alta | Alta (bloqueia o fluxo principal de cadastro de plano) | Aberto |

| **Passo a passo para simular o bug** |
| :--- |
| 1. Acessar o menu "Planos". |
| 2. Clicar em "Novo Plano". |
| 3. Preencher o campo "Nome" corretamente, selecionar um "Grupo" existente, informar 1 parcela e um Valor Mensal (ex.: 50,00). |
| 4. Clicar em "Salvar Plano", sem marcar "Salvar também na Pagar.me". |
| 5. Observar a mensagem "Erro ao salvar plano". |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :--- | :--- |
| O plano deve ser cadastrado com sucesso e aparecer na listagem. | O cadastro falha sempre, com `POST /api/plano/salvar/1` retornando HTTP 500. |

| **Ambiente** |
| :--- |
| Endereço: https://sifitalfa.centrion.com.br/planos |
| Navegador, versão e tipo de ambiente: a registrar. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :--- | :--- |
| Planos — cadastro | C05-CT05: Cadastro de novo plano retorna erro do servidor (RF05 - Planos) |

| **Evidência(s)** |
| :--- |
| Link do vídeo do JAM: a adicionar. |

---

### **Bug 14: Anamnese aplicada com sucesso não aparece na listagem de Fichas Anamnese**

| **ID** | **Descrição** |
| :--- | :--- |
| SIFIT-BUG-014 | Ao concluir o fluxo de "Nova Anamnese" (selecionar aluno, selecionar modelo, responder as perguntas e finalizar), a anamnese é salva com sucesso no backend, mas não aparece na listagem da tela de Fichas Anamnese, que continua exibindo "Nenhuma ficha encontrada" e todos os indicadores zerados. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| :--- |
| 1. Acessar o menu "Fichas Anamnese". |
| 2. Clicar em "Nova Anamnese". |
| 3. Selecionar um aluno e o modelo "Manual SIFIT Anamnese Inicial". |
| 4. Responder a pergunta exibida. |
| 5. Clicar em "Revisar" e depois em "Finalizar Anamnese". |
| 6. Observar que a tela retorna para a listagem, que continua exibindo "Nenhuma ficha encontrada", mesmo após recarregar a página. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :--- | :--- |
| A anamnese finalizada deve aparecer na listagem e nos indicadores da tela. | A requisição `POST /api/anamnese/aplicar/1` retorna HTTP 201 (sucesso), mas a listagem (`POST /api/fichas-anamnese/1`) não retorna o registro recém-criado. |

| **Ambiente** |
| :--- |
| Endereço: https://sifitalfa.centrion.com.br/anamneses |
| Navegador, versão e tipo de ambiente: a registrar. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :--- | :--- |
| Fichas Anamnese — listagem | C08-CT03: Aplicação de uma nova anamnese e exibição na listagem (RF08 - Fichas Anamnese) |

| **Evidência(s)** |
| :--- |
| Link do vídeo do JAM: a adicionar. |

---

### **Bug 15: Não é possível cadastrar nova ficha de treino ("Erro ao salvar Ficha")**

| **ID** | **Descrição** |
| :--- | :--- |
| SIFIT-BUG-015 | O cadastro de uma nova ficha de treino falha com a mensagem "Erro ao salvar Ficha", com o backend retornando HTTP 500, mesmo com aluno e objetivo selecionados corretamente. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Alta | Alta (bloqueia o fluxo principal de criação de ficha de treino) | Aberto |

| **Passo a passo para simular o bug** |
| :--- |
| 1. Acessar o menu "Ficha de Treino". |
| 2. Clicar em "Cadastrar Ficha". |
| 3. Buscar e selecionar um aluno. |
| 4. Selecionar um Objetivo do Treino (ex.: "Manual SIFIT Hipertrofia"). |
| 5. Clicar em "Criar Nova Ficha". |
| 6. Observar a mensagem "Erro ao salvar Ficha". |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :--- | :--- |
| A ficha de treino deve ser criada com sucesso e vinculada ao aluno. | O cadastro falha sempre, com `POST /api/adicionar-ficha/1` retornando HTTP 500. |

| **Ambiente** |
| :--- |
| Endereço: https://sifitalfa.centrion.com.br/fichas-treino |
| Navegador, versão e tipo de ambiente: a registrar. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :--- | :--- |
| Ficha de Treino — cadastro | C10-CT03: Cadastro de nova ficha de treino (RF10 - Ficha de Treino) |

| **Evidência(s)** |
| :--- |
| Link do vídeo do JAM: a adicionar. |

---

### **Bug 16: Mensagem "Erro ao salvar enquete" exibida mesmo com sucesso do backend**

| **ID** | **Descrição** |
| :--- | :--- |
| SIFIT-BUG-016 | Ao cadastrar uma nova enquete, o sistema exibe a mensagem "Erro ao salvar enquete", mesmo quando `POST /api/enquete/salvar/1` retorna HTTP 200 (sucesso) e o registro é de fato criado e aparece na listagem. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| :--- |
| 1. Acessar o menu "Enquetes". |
| 2. Clicar em "Nova Enquete". |
| 3. Preencher Nome, Pergunta e uma Resposta. |
| 4. Clicar em "Salvar". |
| 5. Observar a mensagem "Erro ao salvar enquete". |
| 6. Buscar o nome cadastrado na listagem e confirmar que a enquete foi criada normalmente (com código novo). |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :--- | :--- |
| Uma mensagem de erro só deve ser exibida quando o salvamento de fato falhar. | A mensagem de erro aparece mesmo quando o backend confirma sucesso (HTTP 200) e o registro é criado. |

| **Ambiente** |
| :--- |
| Endereço: https://sifitalfa.centrion.com.br/enquetes |
| Navegador, versão e tipo de ambiente: a registrar. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :--- | :--- |
| Enquetes — cadastro | C27-CT02: Cadastro de enquete com pergunta e resposta (RF27 - Enquetes) |

| **Evidência(s)** |
| :--- |
| Link do vídeo do JAM: a adicionar. |
