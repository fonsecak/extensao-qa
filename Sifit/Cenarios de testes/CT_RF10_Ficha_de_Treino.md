## Cenário 10: Consulta e cadastro de fichas de treino.

### Caso de Teste 01: Acesso à tela de Ficha de Treino.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C10-CT01 | A tela de Ficha de Treino deve apresentar filtros e ações de consulta. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos autenticados no Sifit |
| **QUANDO** clicarmos no menu "Ficha de Treino" |
| **ENTÃO** a tela de Ficha de Treino deve ser exibida |
| **E** devem estar disponíveis os filtros "Código", "Nome do Aluno" e "Status" |
| **E** devem estar disponíveis as ações "Buscar", "Limpar filtros" e "Cadastrar Ficha" |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A tela deve carregar sem apresentar mensagem de erro. |
| Os filtros e as ações descritos devem estar disponíveis. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| [Assistir ao vídeo](../Videos/7.1.mp4)

---

### Caso de Teste 02: Abertura do formulário de Ficha de Treino.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C10-CT02 | O formulário de Ficha de Treino deve apresentar os campos observados. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e na tela de Ficha de Treino. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de Ficha de Treino |
| **QUANDO** clicarmos em "Cadastrar Ficha" |
| **ENTÃO** o formulário de Ficha de Treino deve ser exibido |
| **E** devem estar disponíveis os campos "Código e Nome do aluno", "Personal", "Data Inicial" e "Data Final" |
| **E** devem estar disponíveis os campos "Objetivo" e "Observação" |
| **E** devem estar disponíveis as ações "Pesquisar", "Cancelar", "Criar Nova Ficha" e "Usar Modelo de Ficha" |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| O formulário deve abrir sem apresentar mensagem de erro. |
| Os campos e as ações descritos devem estar disponíveis. |
| O caso verifica a abertura do formulário; não selecionar aluno nem criar ficha. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| [Assistir ao vídeo](../Videos/7.2.mp4)

---

### Caso de Teste 03: Cadastro de nova ficha de treino.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C10-CT03 | O sistema deve permitir criar uma ficha de treino vinculada a um aluno. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| Deve existir um aluno sem ficha de treino ativa. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos no formulário "Cadastrar Ficha de Treino" |
| **QUANDO** buscarmos e selecionarmos um aluno |
| **E** selecionarmos um Objetivo do Treino |
| **E** clicarmos em "Criar Nova Ficha" |
| **ENTÃO** a ficha deve ser criada e vinculada ao aluno |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A ficha deve ser salva com sucesso e aparecer na listagem de Fichas de Treino. |


| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: https://jam.dev/c/2fbed349-8201-4cf2-b7fe-8fd25d316389 |
