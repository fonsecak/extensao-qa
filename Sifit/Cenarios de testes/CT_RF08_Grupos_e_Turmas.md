## Cenário 08: Grupos e Turmas.

### Caso de Teste 01: Acesso e visualização da lista de Grupos.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C08-CT01 | A tela de Grupos deve apresentar os registros cadastrados para consulta. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos autenticados no Sifit |
| **QUANDO** acessarmos o menu "Grupos" |
| **ENTÃO** a tela de Grupos deve ser exibida sem erro |
| **E** os grupos cadastrados devem estar disponíveis para consulta |
| **E** as informações apresentadas na listagem devem corresponder aos registros exibidos |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A tela deve carregar sem apresentar mensagem de erro. |
| A listagem deve apresentar os grupos cadastrados, ou uma indicação de que não há registros. |
| Este caso é somente de consulta; não cadastrar, editar ou excluir registros. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| [Assistir ao vídeo](../Videos/8.1.mp4) |

---

### Caso de Teste 02: Consulta de grupos usando os filtros disponíveis.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C08-CT02 | A consulta de grupos deve apresentar resultados compatíveis com os filtros informados. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e na tela de Grupos. |
| Deve existir um grupo cujo dado de identificação seja conhecido para a consulta. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de Grupos |
| **E** conhecemos um dado de um grupo cadastrado |
| **QUANDO** informarmos esse dado no filtro correspondente disponível na tela e realizarmos a consulta |
| **ENTÃO** o sistema deve apresentar o grupo correspondente ao dado informado |
| **E** os dados exibidos devem corresponder ao grupo consultado |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| O resultado deve corresponder ao dado informado. |
| Se a tela não oferecer filtros, registrar isso na evidência e considerar a listagem apresentada no Caso de Teste 01. |
| A consulta não deve alterar os dados do grupo. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| [Assistir ao vídeo](../Videos/8.2.mp4) |

---

### Caso de Teste 03: Acesso e visualização da lista de Turmas.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C08-CT03 | A tela de Turmas deve apresentar as turmas cadastradas para consulta. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos autenticados no Sifit |
| **QUANDO** acessarmos o menu "Turmas" |
| **ENTÃO** a tela de Turmas deve ser exibida sem erro |
| **E** as turmas cadastradas devem estar disponíveis para consulta |
| **E** as informações apresentadas na listagem devem corresponder aos registros exibidos |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A tela deve carregar sem apresentar mensagem de erro. |
| A listagem deve apresentar as turmas cadastradas, ou uma indicação de que não há registros. |
| Este caso é somente de consulta; não cadastrar, editar ou excluir registros. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| [Assistir ao vídeo](../Videos/8.3.mp4) |

---

### Caso de Teste 04: Consulta de turmas usando os filtros disponíveis.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C08-CT04 | A consulta de turmas deve apresentar resultados compatíveis com os filtros informados. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e na tela de Turmas. |
| Deve existir uma turma cujo dado de identificação seja conhecido para a consulta. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de Turmas |
| **E** conhecemos um dado de uma turma cadastrada |
| **QUANDO** informarmos esse dado no filtro correspondente disponível na tela e realizarmos a consulta |
| **ENTÃO** o sistema deve apresentar a turma correspondente ao dado informado |
| **E** os dados exibidos devem corresponder à turma consultada |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| O resultado deve corresponder ao dado informado. |
| Se a tela não oferecer filtros, registrar isso na evidência e considerar a listagem apresentada no Caso de Teste 03. |
| A consulta não deve alterar os dados da turma. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| [Assistir ao vídeo](../Videos/8.4.mp4) |

---

### Caso de Teste 05: Visualização das informações de uma turma.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C08-CT05 | As informações disponíveis de uma turma devem ser exibidas corretamente para consulta. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e na tela de Turmas. |
| Deve existir uma turma cadastrada com informações disponíveis para consulta. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de Turmas |
| **E** existe uma turma cadastrada |
| **QUANDO** abrirmos os dados dessa turma pela opção de consulta disponível na tela |
| **ENTÃO** as informações da turma devem ser apresentadas |
| **E** devem ser exibidos os participantes, horários e capacidade quando esses dados estiverem disponíveis para a turma |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| Os dados exibidos devem corresponder à turma consultada. |
| Participantes, horários e capacidade devem corresponder às informações apresentadas no cadastro da turma, quando disponíveis. |
| A consulta não deve alterar o cadastro. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| [Assistir ao vídeo](../Videos/8.5.mp4) |
