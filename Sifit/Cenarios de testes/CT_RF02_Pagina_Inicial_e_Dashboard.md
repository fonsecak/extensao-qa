## Cenário 02: Acesso e visualização da Página Inicial e do Dashboard.

### Caso de Teste 01: Acesso e visualização da Página Inicial.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C02-CT01 | A Página Inicial deve apresentar os indicadores e as informações da academia. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos autenticados no Sifit |
| **QUANDO** clicarmos no menu "Página Inicial" |
| **ENTÃO** a Página Inicial deve ser exibida |
| **E** devem ser apresentados os indicadores de clientes, matrículas e mensalidades pendentes |
| **E** devem ser apresentadas as seções de agenda, últimas entradas e aniversariantes |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A Página Inicial deve carregar sem apresentar mensagem de erro. |
| Os indicadores e as seções devem ser exibidos, mesmo quando não houver registros. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: | https://jam.dev/c/097f0a88-4a2f-493d-8193-a4b89442d92d

---

### Caso de Teste 02: Acesso e visualização do Dashboard.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C02-CT02 | O Dashboard deve apresentar as seções disponíveis para o usuário. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos autenticados no Sifit |
| **QUANDO** clicarmos no menu "Dashboard" |
| **ENTÃO** o Dashboard deve ser exibido |
| **E** devem ser apresentadas as seções "Despesas Fixas" e "Inteligência Sifit" |
| **E** o botão "Ver Inteligência" deve estar visível |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| O Dashboard deve carregar sem apresentar mensagem de erro. |
| As seções "Despesas Fixas" e "Inteligência Sifit" e o botão "Ver Inteligência" devem ser exibidos. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: | https://jam.dev/c/d8492524-5dd8-4051-a673-012d47f52750

---

### Caso de Teste 03: Navegação entre a Página Inicial, Clientes e o Dashboard.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C02-CT03 | Os menus devem permitir o acesso às telas correspondentes sem encerrar a sessão. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |
| O usuário deve estar na Página Inicial. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na Página Inicial do Sifit |
| **QUANDO** clicarmos no menu "Clientes" |
| **ENTÃO** a tela de Clientes deve ser exibida com os filtros "Código" e "Nome" e o botão "Buscar" |
| **QUANDO** clicarmos no menu "Dashboard" |
| **ENTÃO** o Dashboard deve ser exibido |
| **QUANDO** clicarmos no menu "Página Inicial" |
| **ENTÃO** devemos retornar à Página Inicial com a sessão autenticada |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| Cada menu deve abrir a tela correspondente sem apresentar mensagem de erro. |
| O usuário deve permanecer autenticado durante a navegação. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: | https://jam.dev/c/d8492524-5dd8-4051-a673-012d47f52750
