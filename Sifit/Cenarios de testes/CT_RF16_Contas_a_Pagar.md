## Cenário 16: Consulta de Contas a Pagar.

### Caso de Teste 01: Acesso e visualização de Contas a Pagar.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C16-CT01 | A tela de Contas a Pagar deve apresentar os registros financeiros disponíveis para consulta. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos autenticados no Sifit |
| **QUANDO** acessarmos o menu "Contas a Pagar" |
| **ENTÃO** a tela deve ser exibida sem mensagem de erro |
| **E** os registros disponíveis devem ser apresentados para consulta |
| **E** valores, datas e situações devem estar visíveis quando disponíveis na listagem |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A tela deve carregar sem apresentar mensagem de erro. |
| Os registros devem ser exibidos ou o sistema deve indicar que não há registros para apresentar. |
| Este caso é somente de consulta; não pagar contas nem alterar lançamentos. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| [Assistir ao vídeo](../Videos/9.3.mp4) |

---

### Caso de Teste 02: Consulta e conferência de Contas a Pagar.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C16-CT02 | Os filtros disponíveis devem apresentar contas a pagar compatíveis com os critérios informados. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e na tela de Contas a Pagar. |
| Deve existir um registro financeiro autorizado para consulta, com dados conhecidos para conferência. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de Contas a Pagar |
| **E** conhecemos um dado do registro que será consultado |
| **QUANDO** informarmos o critério nos filtros disponíveis e realizarmos a consulta |
| **ENTÃO** o sistema deve apresentar os registros correspondentes ao critério informado |
| **E** devemos conferir valor, data e situação com o registro consultado, quando disponíveis |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| Os resultados devem corresponder aos critérios utilizados. |
| Valores, datas e situações apresentados devem corresponder ao registro consultado. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| [Assistir ao vídeo](../Videos/9.4.mp4) |
