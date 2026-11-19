## Cenário 22: Consulta e cadastro de Tipos de Pagamento e Bandeiras de Cartão.

### Caso de Teste 01: Acesso à tela de Tipos de Pagamento.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C22-CT01 | A tela de Tipos de Pagamento deve apresentar a lista de tipos e permitir a busca por nome. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos autenticados no Sifit |
| **QUANDO** clicarmos no menu "Tipos de Pagamento" |
| **ENTÃO** a tela deve ser exibida com os indicadores "Total", "Crédito", "Débito" e "Via gateway" |
| **QUANDO** informarmos o nome de um tipo existente no campo "Nome" e clicarmos em "Buscar" |
| **ENTÃO** os tipos correspondentes devem ser exibidos com a contagem de registros |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A tela deve carregar sem apresentar mensagem de erro. |
| A busca por nome deve retornar os registros correspondentes. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: a adicionar. |

---

### Caso de Teste 02: Cadastro de nova Bandeira de Cartão.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C22-CT02 | A tela de Bandeiras de Cartão deve apresentar a lista de bandeiras e permitir o cadastro de uma nova, com validação do campo obrigatório. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos autenticados no Sifit |
| **QUANDO** clicarmos no menu "Bandeiras" |
| **ENTÃO** a tela de Bandeiras de Cartão deve ser exibida |
| **QUANDO** clicarmos em "Nova Bandeira" |
| **ENTÃO** o formulário deve apresentar os campos "Código", "Nome", "Taxa Adicional", "Taxa Débito" e a tabela de "Parcelas" |
| **QUANDO** clicarmos em "Salvar" sem informar o nome |
| **ENTÃO** o sistema deve apresentar um aviso informando que o nome da bandeira é obrigatório |
| **QUANDO** preenchermos o nome e clicarmos em "Salvar" |
| **ENTÃO** a bandeira deve ser criada e listada na tela |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A listagem deve indicar corretamente quando não houver registros. |
| A validação do campo "Nome" deve impedir o cadastro sem preenchimento. |
| A bandeira deve aparecer na listagem imediatamente após o cadastro. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: a adicionar. |
