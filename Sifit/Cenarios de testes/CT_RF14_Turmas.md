## Cenário 14: Consulta de Turmas.

### Caso de Teste 01: Acesso e visualização da lista de Turmas.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C14-CT01 | A tela de Turmas deve apresentar as turmas cadastradas para consulta. |

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

### Caso de Teste 02: Consulta de turmas usando os filtros disponíveis.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C14-CT02 | A consulta de turmas deve apresentar resultados compatíveis com os filtros informados. |

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
| Se a tela não oferecer filtros, registrar isso na evidência e considerar a listagem apresentada no Caso de Teste 01. |
| A consulta não deve alterar os dados da turma. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| [Assistir ao vídeo](../Videos/8.4.mp4) |

---

### Caso de Teste 03: Visualização das informações de uma turma.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C14-CT03 | As informações disponíveis de uma turma devem ser exibidas corretamente para consulta. |

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

---

### Caso de Teste 04: Cadastro e exclusão de Turma.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C14-CT04 | O sistema deve permitir cadastrar uma nova turma, com validação de dias da semana obrigatórios, e excluí-la em seguida. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos no formulário "Cadastrar Turma" |
| **QUANDO** preenchermos Nome e Plano, sem marcar dia da semana, e clicarmos em "Salvar" |
| **ENTÃO** o sistema deve exigir "Selecione ao menos um dia da semana" |
| **QUANDO** marcarmos um dia e salvarmos novamente |
| **ENTÃO** a turma deve ser criada; excluída em seguida pela ação de deletar |

| **Resultado obtido** |
| :-------------------------------------------------------------- |
| Validação e cadastro funcionaram corretamente. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: https://jam.dev/c/4353edba-33af-42f8-9793-7164296d9ac4 |
