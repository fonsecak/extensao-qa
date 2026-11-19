## Cenário 13: Consulta de Grupos.

### Caso de Teste 01: Acesso e visualização da lista de Grupos.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C13-CT01 | A tela de Grupos deve apresentar os registros cadastrados para consulta. |

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
| C13-CT02 | A consulta de grupos deve apresentar resultados compatíveis com os filtros informados. |

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

### Caso de Teste 03: Cadastro e exclusão de Grupo.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C13-CT03 | O sistema deve permitir cadastrar um novo grupo e excluí-lo em seguida. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e no formulário de novo grupo. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos no formulário "Novo Grupo" |
| **QUANDO** preenchermos o campo "Nome" |
| **E** clicarmos em "Salvar Grupo" |
| **ENTÃO** o grupo deve ser criado e listado |
| **QUANDO** buscarmos esse grupo e clicarmos em excluir, confirmando |
| **ENTÃO** o grupo deve ser removido da listagem |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| O cadastro e a exclusão devem ser concluídos com sucesso, e o indicador "Grupos" deve refletir a mudança. |

| **Resultado obtido** |
| :-------------------------------------------------------------- |
| Cadastro funcionou, mas houve erro na exclusão do Grupo cadastrado  |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: https://jam.dev/c/ef249d6e-87df-4ac9-9c68-94d48d28d7de |
