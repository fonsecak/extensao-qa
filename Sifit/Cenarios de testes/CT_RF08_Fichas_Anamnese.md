## Cenário 08: Consulta e aplicação de fichas de anamnese.

### Caso de Teste 01: Acesso à tela de Fichas Anamnese.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C08-CT01 | A tela de Fichas Anamnese deve apresentar a busca e a opção de nova anamnese. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos autenticados no Sifit |
| **QUANDO** clicarmos no menu "Fichas Anamnese" |
| **ENTÃO** a tela de Fichas Anamnese deve ser exibida |
| **E** deve estar disponível a busca por cliente |
| **E** deve estar disponível a ação "Nova Anamnese" |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A tela de Fichas Anamnese deve carregar sem apresentar mensagem de erro. |
| A busca e a ação "Nova Anamnese" devem estar disponíveis. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link:  https://jam.dev/c/ceb02381-78af-44e8-a599-efbac11d7b6e |

---

### Caso de Teste 02: Abertura do fluxo de aplicação de anamnese.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C08-CT02 | O fluxo de nova anamnese deve iniciar pela seleção do aluno. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e na tela de Fichas Anamnese. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de Fichas Anamnese |
| **QUANDO** clicarmos em "Nova Anamnese" |
| **ENTÃO** o primeiro passo para aplicar anamnese deve ser exibido |
| **E** deve estar disponível a busca pelo nome do aluno |
| **E** deve ser apresentada a etapa "Selecionar Aluno" e a ação "Próxima" |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| O primeiro passo deve abrir sem apresentar mensagem de erro. |
| A busca do aluno, a etapa e a ação descritas devem estar disponíveis. |
| O caso verifica o primeiro passo; não selecionar aluno nem avançar. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link:  https://jam.dev/c/eee96adc-dd9c-4464-8f1c-6e2fd3aabb50 |

---

### Caso de Teste 03: Aplicação de uma nova anamnese e exibição na listagem.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C08-CT03 | O sistema deve permitir aplicar uma anamnese completa a um cliente e exibi-la na listagem. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| Deve existir um modelo de anamnese cadastrado com ao menos uma pergunta. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos no fluxo de nova anamnese |
| **QUANDO** selecionarmos um aluno e um modelo |
| **E** respondermos a(s) pergunta(s) do modelo |
| **E** clicarmos em "Revisar" e depois em "Finalizar Anamnese" |
| **ENTÃO** a anamnese deve ser salva e exibida na listagem de Fichas Anamnese |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A anamnese finalizada deve aparecer na listagem, e o indicador "Total de fichas" deve ser incrementado. |

| **Resultado obtido** |
| :-------------------------------------------------------------- |
| A anamnese foi aplicada com sucesso no backend (`POST /api/anamnese/aplicar/1` retornou HTTP 201), mas a listagem de Fichas Anamnese continua exibindo "Nenhuma ficha encontrada" e todos os indicadores em 0, mesmo após recarregar a página. Falha registrada em SIFIT-BUG-014. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: https://jam.dev/c/13ebc4d2-61ff-4d83-8eca-bfa623a4bbec |
