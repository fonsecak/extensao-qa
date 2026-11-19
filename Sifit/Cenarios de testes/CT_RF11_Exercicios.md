## Cenário 11: Consulta e cadastro de exercícios.

### Caso de Teste 01: Acesso à biblioteca de Exercícios.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C11-CT01 | A biblioteca de Exercícios deve ser exibida organizada por grupos musculares. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos autenticados no Sifit |
| **QUANDO** clicarmos no menu "Exercícios" |
| **ENTÃO** a biblioteca de exercícios deve ser exibida |
| **E** os exercícios devem estar organizados por grupos musculares |
| **E** deve estar disponível a ação "Adicionar" |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A biblioteca deve carregar sem apresentar mensagem de erro. |
| A organização por grupos musculares e a ação "Adicionar" devem estar disponíveis. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| [Assistir ao vídeo](../Videos/7.3.mp4)

---

### Caso de Teste 02: Abertura do formulário de exercício.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C11-CT02 | O formulário de exercício deve apresentar os campos de cadastro observados. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e na tela de Exercícios. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na biblioteca de Exercícios |
| **QUANDO** clicarmos em "Adicionar" |
| **ENTÃO** o formulário de exercício deve ser exibido |
| **E** o campo "Nome" deve estar identificado como obrigatório |
| **E** devem estar disponíveis os campos "Código", "Imagem" e "Vídeo" |
| **E** devem estar disponíveis as ações "Fechar", "Cancelar" e "Salvar" |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| O formulário deve abrir sem apresentar mensagem de erro. |
| Os campos e as ações descritos devem estar disponíveis. |
| O caso verifica a abertura do formulário; não enviar arquivos nem salvar o exercício. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| [Assistir ao vídeo](../Videos/7.4.mp4)

---

### Caso de Teste 03: Cadastro e exclusão de exercício.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C11-CT03 | O sistema deve permitir cadastrar um novo exercício em um grupo muscular e excluí-lo em seguida. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| Deve existir ao menos um grupo muscular cadastrado. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na biblioteca de Exercícios |
| **QUANDO** clicarmos em "Adicionar" em um grupo muscular |
| **E** preenchermos o campo "Nome" |
| **E** clicarmos em "Salvar" |
| **ENTÃO** o exercício deve ser criado e listado no grupo |
| **QUANDO** clicarmos na ação de excluir desse exercício e confirmarmos |
| **ENTÃO** o exercício deve ser removido do grupo |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| O cadastro e a exclusão devem refletir corretamente no contador "Total" e na listagem do grupo. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: a adicionar. |
