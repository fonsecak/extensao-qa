## Cenário 21: Consulta e cadastro de Modelos de Contrato.

### Caso de Teste 01: Acesso à tela de Modelos de Contrato.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C21-CT01 | A tela de Modelos de Contrato deve apresentar a lista de modelos e a ação de criação. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos autenticados no Sifit |
| **QUANDO** clicarmos no menu "Modelos Contrato" |
| **ENTÃO** a tela de Modelos de Contrato deve ser exibida |
| **E** devem estar disponíveis as colunas "Código", "Nome" e "Status" |
| **E** deve estar disponível a ação "Adicionar Modelo Contrato" |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A tela deve carregar sem apresentar mensagem de erro. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: a adicionar. |

---

### Caso de Teste 02: Edição de modelo de contrato com variáveis dinâmicas.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C21-CT02 | O editor de modelo de contrato deve permitir inserir variáveis e atualizar a pré-visualização. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e na tela de Modelos de Contrato. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos no editor de um novo modelo de contrato |
| **E** digitamos um texto no campo "Texto do contrato" |
| **QUANDO** clicarmos em uma variável disponível, como "{nome_aluno}" |
| **ENTÃO** a variável deve ser inserida no texto do contrato |
| **QUANDO** clicarmos em "Atualizar preview" |
| **ENTÃO** a pré-visualização deve exibir o texto com a variável substituída por um valor de exemplo |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A variável deve ser inserida corretamente na posição do cursor. |
| A pré-visualização deve refletir o texto do contrato com as variáveis resolvidas. |
| O caso verifica a edição e a pré-visualização; não salvar o modelo. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: a adicionar. |
