## Cenário 20: Consulta e cadastro de leads na Prospecção.

### Caso de Teste 01: Acesso à tela de Prospecção.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C20-CT01 | A tela de Prospecção deve apresentar a lista de leads e os indicadores do funil. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos autenticados no Sifit |
| **QUANDO** clicarmos no menu "Prospecção" |
| **ENTÃO** a tela de Prospecção deve ser exibida |
| **E** devem ser apresentados os indicadores "Leads", "Novos Contatos" e "Interessados" |
| **E** deve ser exibida a lista de leads com código, nome, estágio e data de criação |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A tela deve carregar sem apresentar mensagem de erro. |
| Os indicadores devem refletir os registros exibidos na lista. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: https://jam.dev/c/fe765a66-655a-4833-af8e-e32aee2f76fd |

---

### Caso de Teste 02: Busca de lead por nome.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C20-CT02 | A busca pelo campo "Buscar lead" deve localizar leads pelo nome informado. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e na tela de Prospecção. |
| Deve existir ao menos um lead cadastrado. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de Prospecção |
| **E** identificamos o nome de um lead já listado |
| **QUANDO** informarmos esse nome no campo "Buscar lead" |
| **ENTÃO** o lead correspondente deve ser exibido na lista |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| O campo indica que aceita "Nome, e-mail, telefone ou código"; a busca por nome deve retornar o lead correspondente. |

| **Resultado obtido** |
| :-------------------------------------------------------------- |
| A busca pelo nome completo ou parcial do lead não retorna nenhum resultado, mesmo quando o lead está listado na tela. A busca pelo código funciona normalmente. Falha registrada em SIFIT-BUG-003. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: https://jam.dev/c/e041ee04-9ea5-4f94-9781-625cfbb0ab81 |

---

### Caso de Teste 03: Busca de lead por código e limpeza do filtro.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C20-CT03 | A busca por código deve localizar o lead e a ação "Limpar" deve restaurar a lista completa. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e na tela de Prospecção. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de Prospecção |
| **QUANDO** informarmos o código de um lead existente no campo "Buscar lead" |
| **ENTÃO** apenas o lead correspondente deve ser exibido |
| **QUANDO** clicarmos em "Limpar" |
| **ENTÃO** a lista completa de leads deve ser restaurada |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A busca por código deve retornar o resultado correto. |
| A ação "Limpar" deve remover o filtro aplicado. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: https://jam.dev/c/d4da108d-f9aa-4429-930c-c4ffd617bc51 |

---

### Caso de Teste 04: Cadastro de novo lead.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C20-CT04 | O sistema deve permitir cadastrar um novo lead, com validação do campo obrigatório. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e na tela de Prospecção. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de Prospecção |
| **QUANDO** clicarmos em "Adicionar Lead" |
| **ENTÃO** o formulário deve ser exibido com os campos "Nome", "Estágio do Lead", "E-mail", "Telefone" e "Observação" |
| **QUANDO** clicarmos em "Salvar Lead" sem preencher o nome |
| **ENTÃO** o sistema deve apresentar a mensagem "Preencha este campo" |
| **QUANDO** preenchermos o nome e clicarmos em "Salvar Lead" |
| **ENTÃO** o lead deve ser criado e listado na tela de Prospecção |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A validação do campo obrigatório "Nome" deve impedir o envio sem preenchimento. |
| O lead deve aparecer na listagem imediatamente após o cadastro. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: https://jam.dev/c/bae16ab2-11ce-4ea1-b9fa-1108bd00cf27 |
