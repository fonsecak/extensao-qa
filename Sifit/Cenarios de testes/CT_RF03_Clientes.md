## Cenário 03: Consulta e cadastro de clientes.

### Caso de Teste 01: Acesso à tela de Clientes.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C03-CT01 | A tela de Clientes deve apresentar os filtros e a opção de cadastro. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos autenticados no Sifit |
| **QUANDO** clicarmos no menu "Clientes" |
| **ENTÃO** a tela de Clientes deve ser exibida |
| **E** devem estar disponíveis os filtros Código, Nome, Status, Situação, Plano e Personal |
| **E** devem estar disponíveis os botões "Buscar" e "Novo Cliente" |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A tela de Clientes deve carregar sem apresentar mensagem de erro. |
| Os filtros e os botões observados no levantamento devem estar disponíveis. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: | https://jam.dev/c/fe82f8e3-90fb-44a6-ad2a-fafb9a3a2215

---

### Caso de Teste 02: Busca de cliente pelo nome.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C03-CT02 | A busca deve retornar o cliente correspondente ao nome informado. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e na tela de Clientes. |
| Deve existir um cliente de teste conhecido e autorizado para consulta. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de Clientes |
| **E** informamos o nome conhecido no filtro "Nome" |
| **QUANDO** clicarmos no botão "Buscar" |
| **ENTÃO** o sistema deve apresentar o cliente correspondente ao nome informado |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| O resultado deve corresponder ao nome utilizado na busca. |
| Os dados exibidos devem corresponder ao cliente de teste consultado. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: | https://jam.dev/c/fe82f8e3-90fb-44a6-ad2a-fafb9a3a2215

---

### Caso de Teste 03: Abertura do formulário de novo cliente.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C03-CT03 | O formulário de novo cliente deve apresentar os campos obrigatórios. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e na tela de Clientes. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de Clientes |
| **QUANDO** clicarmos no botão "Novo Cliente" |
| **ENTÃO** o formulário de cadastro de cliente deve ser exibido |
| **E** os campos Nome, Status, Sexo e Data de Nascimento devem estar identificados como obrigatórios |
| **E** devem estar disponíveis as opções "Cancelar" e salvar o cadastro |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| O formulário de novo cliente deve abrir sem apresentar mensagem de erro. |
| Nome, Status, Sexo e Data de Nascimento devem estar identificados como obrigatórios. |
| O caso verifica a abertura do formulário; não salvar o cadastro durante este teste. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: | https://jam.dev/c/0032de48-b2bf-47f0-bfe4-481e3f7c641f
