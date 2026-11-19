## Cenário 18: Consulta de Despesas Fixas.

### Caso de Teste 01: Acesso e visualização de Despesas Fixas.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C18-CT01 | A tela de Despesas Fixas deve apresentar os registros disponíveis para consulta. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos autenticados no Sifit |
| **QUANDO** acessarmos o menu "Despesas Fixas" |
| **ENTÃO** a tela deve ser exibida sem mensagem de erro |
| **E** as despesas fixas disponíveis devem ser apresentadas para consulta |
| **E** os valores, datas e situações devem estar visíveis quando disponíveis |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A tela deve carregar sem apresentar mensagem de erro. |
| Os registros devem ser exibidos ou o sistema deve indicar que não há registros para apresentar. |
| Este caso é somente de consulta; não cadastrar, editar ou excluir despesas. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| [Assistir ao vídeo](../Videos/9.7.mp4) |

---

### Caso de Teste 02: Consulta e conferência de Despesas Fixas.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C18-CT02 | Os filtros disponíveis devem apresentar despesas fixas compatíveis com os critérios informados. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e na tela de Despesas Fixas. |
| Deve existir uma despesa fixa autorizada para consulta, com dados conhecidos para conferência. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de Despesas Fixas |
| **E** conhecemos um dado da despesa fixa que será consultada |
| **QUANDO** informarmos o critério nos filtros disponíveis e realizarmos a consulta |
| **ENTÃO** o sistema deve apresentar as despesas correspondentes ao critério informado |
| **E** devemos conferir valor, data e situação com o registro consultado, quando disponíveis |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| Os resultados devem corresponder aos critérios utilizados. |
| Valores, datas e situações apresentados devem corresponder à despesa consultada. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| [Assistir ao vídeo](../Videos/9.8.mp4) |
