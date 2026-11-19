## Cenário 23: Consulta de Colaboradores e Funções.

### Caso de Teste 01: Acesso à tela de Colaboradores.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C23-CT01 | A tela de Colaboradores deve apresentar a lista e permitir a busca por nome. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos autenticados no Sifit |
| **QUANDO** clicarmos no menu "Colaboradores" |
| **ENTÃO** a tela deve ser exibida com os indicadores "Colaboradores Cadastrados", "Colaboradores Ativos" e "Personais" |
| **QUANDO** informarmos o nome de um colaborador existente e clicarmos em "Buscar" |
| **ENTÃO** o colaborador correspondente deve ser exibido |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A tela deve carregar sem apresentar mensagem de erro. |
| A busca por nome deve retornar o registro correto. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: a adicionar. |

---

### Caso de Teste 02: Acesso à tela de Funções.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C23-CT02 | A tela de Funções deve apresentar a lista com os indicadores de Personal e Avaliador. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos autenticados no Sifit |
| **QUANDO** clicarmos no menu "Funções" |
| **ENTÃO** a tela deve ser exibida com os indicadores "Funções", "Internas", "Personal" e "Avaliadores" |
| **E** a lista deve apresentar o tipo da função e as colunas "Personal" e "Avaliador" |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A tela deve carregar sem apresentar mensagem de erro. |
| Os indicadores devem refletir os registros exibidos na lista. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: a adicionar. |
