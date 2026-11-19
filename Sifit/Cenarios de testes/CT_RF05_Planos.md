## Cenário 05: Consulta e cadastro de planos.

### Caso de Teste 01: Acesso e busca de planos.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C05-CT01 | A tela de Planos deve permitir consultar planos pelos filtros disponíveis. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos autenticados no Sifit |
| **QUANDO** clicarmos no menu "Planos" |
| **ENTÃO** a tela de Planos deve ser exibida com os filtros "Código", "Nome" e "Status" |
| **E** devem estar disponíveis as ações "Buscar" e "Novo Plano" |
| **QUANDO** informarmos o nome de um plano de teste conhecido no filtro "Nome" e clicarmos em "Buscar" |
| **ENTÃO** o sistema deve apresentar o plano correspondente ao nome informado |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A tela deve carregar sem apresentar mensagem de erro. |
| Os filtros e as ações descritos devem estar disponíveis. |
| A busca deve apresentar o plano correspondente ao nome utilizado. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link:  https://jam.dev/c/e585dca2-d7a1-4d6b-9083-c07768215220 |

---

### Caso de Teste 02: Abertura do formulário de novo plano.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C05-CT02 | O formulário de plano deve apresentar os campos de cadastro observados. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e na tela de Planos. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de Planos |
| **QUANDO** clicarmos em "Novo Plano" |
| **ENTÃO** o formulário de plano deve ser exibido |
| **E** devem estar disponíveis os campos "Nome", "Grupo", "Status", "Cobrança", "Parcelas", "Valor Mensal" e "Valor Matrícula" |
| **E** deve estar disponível a ação "Salvar Plano" |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| O formulário deve abrir sem apresentar mensagem de erro. |
| Os campos descritos devem estar disponíveis. |
| O caso verifica a abertura do formulário; não salvar o plano nem selecionar a opção "Salvar também na Pagar.me". |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link:  https://jam.dev/c/e585dca2-d7a1-4d6b-9083-c07768215220 |

---

### Caso de Teste 03: Cadastro de novo plano.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C05-CT03 | O sistema deve permitir o cadastro completo de um novo plano, sem integração com o Pagar.me. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e na tela de Planos. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos no formulário de novo plano |
| **QUANDO** preenchermos Nome, Status, Cobrança, Parcelas, Valor Mensal e Valor Matrícula |
| **E** clicarmos em "Salvar Plano", sem marcar a opção de salvar também na Pagar.me |
| **ENTÃO** o plano deve ser criado e listado na tela de Planos |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| O plano deve aparecer na listagem imediatamente após o cadastro. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: https://jam.dev/c/724d4722-7ffa-4242-ae48-5042683b376d |

---

### Caso de Teste 04: Associação incorreta dos campos "Código" e "Nome" no formulário.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C05-CT04 | Os rótulos "Código" e "Nome" do formulário de plano devem corresponder aos campos de entrada corretos. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e no formulário de novo plano. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos no formulário "Novo Plano" |
| **QUANDO** inspecionarmos os campos sob os rótulos "Código" e "Nome" |
| **ENTÃO** o campo abaixo do rótulo "Código" deve corresponder ao identificador do plano |
| **E** o campo abaixo do rótulo "Nome" deve corresponder ao nome do plano |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A estrutura de acessibilidade do formulário (rótulo associado ao campo) deve corresponder à disposição visual. |

| **Resultado obtido** |
| :-------------------------------------------------------------- |
| Os dois campos de texto do bloco "Dados do Plano" não possuem rótulo (`label`) associado corretamente ao campo de entrada. O primeiro campo do formulário (visualmente sob "Código") recebe o foco e o texto digitado quando se tenta preencher o campo "Nome" por meio de ferramentas de acessibilidade ou automação, revelando que a ordem dos elementos no DOM não corresponde à ordem visual ou que os rótulos não estão associados via atributo `for`/`id` ou `aria-label`. Falha registrada em SIFIT-BUG-012. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: a adicionar. |
